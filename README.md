# 3 Easy Tricks To Boost Angular Code Readability

Trick | Benefit
----- | -------
Static Render Method | You can have logic on top, template at the bottom. (If that you don't work with separate template files.)
Directives Indentation | You can easily tell where all the Angular "special code" are located.
Callback Naming Conventions | You can tell what the code's doing simply by looking at the method names.

## Static Render Method
![Static Render Method](https://github.com/dryvid/angular-readability/blob/master/img/render.png?raw=true)

1. Create a static method in your component that returns the template string
2. Use that static method in the component decorator.

If you like to have logic and template on the same page, this trick will make your code easier to follow, because data initially flows from the logic to the template.

## Static Render Method
![Directives Indentation](https://github.com/dryvid/angular-readability/blob/master/img/indent-1.png?raw=true)

![Directives Indentation](https://github.com/dryvid/angular-readability/blob/master/img/indent-2.png?raw=true)

## Callback Naming Conventions

![Callback Naming Conventions](https://github.com/dryvid/angular-readability/blob/master/img/naming.png?raw=true)

What | Naming Convention | e.g.
---- | ----------------- | ----
Callback that listens to a child component output | Prefixed by `to` to differentiate from the `on` callbacks | `toAddPost`
`Output` `EventEmitter` | Prefixed by `output` and followed by a noun term | `outputFormData`
`Output` `EventEmitter` for passing data from a child component output to the parent component | Prefixed by `passUp` as if the component is saying "I'm simply passing up the data, it's not from me." | `passUpFormData`

Basically, callbacks that are not "triggered" by the component itself get the `to` prefix instead of the typical `on`. And having special prefixes like `output` and `passUp` for `EventEmitter` properties makes your template code easier to understand.
