# Component/Module Template
This repository serves as a template for creating new components and modules for Co-op Frontend Toolkit.

## Create a component/module
The steps below will help you set up a new project and kickstart building a new component or module.

### 1. Pick a name for your project
Use the following naming convention:
```
@coopdigital/component-{name}
@coopdigital/module-{name}
```
Example:
```
@coopdigital/component-button
@coopdigital/module-typography
```

### 2. Clone this repository to your prefered location:  
```bash
$ git clone https://github.com/coopdigital/component-template.git ./@coopdigital/module-typography
```

### 3. Prepare a new repository
1. Re-initialise this as a fresh Git repository with `npm run init`.
2. Add your chosen project name to `package.json` along with the `@coopdigital` namespace.
3. Install build tools via `npm install`.
4. Start coding!

## Commands
This package has some useful built-in commands to help you with development:
```bash
$ npm run comb      # runs CSSComb to make your CSS look and read beautifully
$ npm run line      # runs StyleLint against your CSS using `standard` config
$ npm run test      # runs both `comb` and `lint` sequentially to help you test your CSS
```

## Developing Components
All components are name spaced with:
```css
.coop-c-[name]
```

We build our components based on the [BEM style](http://getbem.com/). This combination of name spacing and BEM allows us to build flexible components that can be shared across the Co-op easily - avoiding clashing styles or the need to create complex overrides when developing services.

If you are building a component for the design system you would name space your component with `coop-c-[name]`.

When developing components for specific services choose a sensible namespace for your service. For example Funeral Care components would be named `fc-c-`.

## Extending Components
If you use a global component but want to change it's styling, use extra classes to extend it. For example if you wanted to centre align the text in card, you would add a modifier class (as per BEM) to change the alignment.  Note that the override class uses the name space from the fictional funeral care service built on top of the base components.
```css
.fc-c-card__content--centre {
  text-align: center;
}
```
