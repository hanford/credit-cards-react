Credit Cards React
===

This is a fork of [react-credit-cards](https://github.com/amarofashion/react-credit-cards) without the sass dependency for 100% functionality with css-in-js

A modern credit card component for React.

![demo](https://raw.githubusercontent.com/amarofashion/react-credit-cards/master/docs/media/rccs.gif)

[Demo](https://amarofashion.github.io/react-credit-cards/)

### Install
```
npm install --save react-credit-cards
```

### Usage

```jsx
    import Cards from 'react-credit-cards';
    ...

    <Cards
      number={input.number.value}
      name={input.name.value}
      expiry={input.expiry.value}
      cvc={input.cvc.value}
      focused={state.focused}
    />
```

Don't forget to import the `react-credit-cards/lib/styles.scss` in your main.scss file or import it directly in your component if you are using webpack.

### Features

- We support all credit card issuers available in [Payment](https://github.com/jessepollak/payment) plus Hipercard (a brazilian credit card).

## Props

- `name` {string}: Name on card. *
- `number` {string|number}: Card number. *
- `expiry` {string|number}: Card expiry date. `10/20` or `012017` *
- `cvc` {string|number}: Card CVC/CVV. *
- `focused` {string}: Focused card field. `name|number|expiry|cvc`
- `locale` {object}: Localization text (e.g. `{ valid: 'valid thru' }`).
- `placeholders` {object}: Placeholder text (e.g. `{ name: 'YOUR NAME HERE' }`).
- `preview` {bool}: To use the card to show scrambled data (e.g. `**** 4567`).
- `issuer` {string}: Set the issuer for the `preview` mode (e.g. `visa|mastercard|...`)
- `acceptedCards` {array}: If you want to limit the accepted cards. (e.g. `['visa', 'mastercard']`
- `callback` {func}: A callback function that will be called when the card number has changed with 2 paramaters: `type ({ issuer: 'visa', maxLength: 19 }), isValid ({boolean})`

\* *Required fields*


## Development

Here's how you can get started developing locally:

    $ git clone git@github.com:amarofashion/react-credit-cards.git
    $ cd react-credit-cards
    $ npm install
    $ npm start

Now, if you go to `http://localhost:3000` in your browser, you should see the demo page.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process of contributing to the project.

## Useful links
[EBANK's test numbers](https://www.ebanx.com/business/en/developers/integrations/testing/credit-card-test-numbers)
[Adyen's test numbers](https://gist.github.com/j3j5/8b3e48ccad746b90a54a)
[Worldpay's test card numbers](https://support.worldpay.com/support/kb/bg/testandgolive/tgl5103.html)
[Brazilian cards patterns](https://github.com/erikhenrique/bin-cc/blob/master/README.md)

## LICENSE

This project is licensed under the [MIT License](LICENSE.md).
