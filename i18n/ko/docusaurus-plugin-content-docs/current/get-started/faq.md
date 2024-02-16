---
sidebar_position: 20
pagination_next: guides/index
---

# FAQ

:::info

You can ask your question in our [Telegram chat][telegram], [Discord community][discord], and [GitHub Discussions][github-discussions].

:::

### Is there a toolkit or a linter?

There is an official ESLint config — [@feature-sliced/eslint-config][eslint-config-official], and an ESLint plugin — [@conarti/eslint-plugin-feature-sliced][eslint-plugin-conarti], created by Aleksandr Belous, a community member. You're welcome to contribute to these projects or start your own!

### Where to store the layout/template of pages?

If you need plain markup layouts, you can keep them in `shared/ui`. If you need to use higher layers inside, there are a few options:

- Perhaps you don't need layouts at all? If the layout is only a few lines, it might be reasonable to duplicate the code in each page rather than try to abstract it.
- If you do need layouts, you can have them as separate widgets or pages, and compose them in your router configuration in App. Nested routing is another option.

### What is the difference between a feature and an entity?

An _entity_ is a real-life concept that your app is working with. A _feature_ is an nteraction that provides real-life value to your app’s users, the thing people want to do with your entities.

For more information, along with examples, see the Reference page on [slices][reference-entities].

### Can I embed pages/features/entities into each other?

Yes, but this embedding should happen in higher layers. For example, inside a widget, you can import both features and then insert one feature into another as props/children.

You cannot import one feature from another feature, this is prohibited by the [**import rule on layers**][import-rule-layers].

### What about Atomic Design?

The current version of the methodology does not require nor prohibit the use of Atomic Design together with Feature-Sliced Design.

For example, Atomic Design [can be applied well](https://t.me/feature_sliced/1653) for the `ui` segment of modules.

### Are there any useful resources/articles/etc. about FSD?

Yes! https://github.com/feature-sliced/awesome

### Why do I need Feature-Sliced Design?

It helps you and your team to quickly overview the project in terms of its main value-bringing components. A standardized architecture helps to speed up onboarding and resolves debates about code structure. See the [motivation][motivation] page to learn more about why FSD was created.

### Does a novice developer need an architecture/methodology?

Rather yes than no

*Usually, when you design and develop a project in one person, everything goes smoothly. But if there are pauses in development, new developers are added to the team - then problems come*

### How do I work with the authorization context?

Answered [here](/docs/guides/examples/auth)

[import-rule-layers]: /docs/reference/layers#import-rule-on-layers
[reference-entities]: /docs/reference/layers#entities
[eslint-config-official]: https://github.com/feature-sliced/eslint-config
[eslint-plugin-conarti]: https://github.com/conarti/eslint-plugin-feature-sliced
[motivation]: /docs/about/motivation
[telegram]: https://t.me/feature_sliced
[discord]: https://discord.gg/S8MzWTUsmp
[github-discussions]: https://github.com/feature-sliced/documentation/discussions
