# formik-adapter-zod

## Works with react v18

This library adapts a [zod](https://www.npmjs.com/package/zod) schema to work as a `validationSchema` prop on [Formik](https://www.npmjs.com/package/formik)

**IMPORTANT: Currently, this library does not work with zod union. See more [here](https://github.com/lukem121/formik-adapter-zod/issues/2).**

## Install

```sh
# npm
$ npm install formik-adapter-zod

# yarn
$ yarn add formik-adapter-zod
```

## Usage

```TSX
import { z } from 'zod';
import { Formik } from 'formik';
import { toFormikValidationSchema } from 'formik-adapter-zod';

const Schema = z.object({
  name: z.string(),
  age: z.number(),
});

const Component = () => (
  <Formik
    validationSchema={toFormikValidationSchema(Schema)}
  >
    {...}
  </Formik>
);
```
