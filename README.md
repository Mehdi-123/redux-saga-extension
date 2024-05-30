# Redux Saga Features Generator

Redux Saga Features Generator is a Visual Studio Code extension that provides code snippets to help you quickly generate Redux Saga related boilerplate code. This extension aims to streamline the process of setting up actions, constants, reducers, sagas, and selectors for new features in your Redux applications.

## Features

This extension includes snippets for:

- **Constants**: Generate action type constants for your Redux actions.
- **Actions**: Generate action creators for your Redux actions.
- **Reducers**: Generate switch case blocks for handling Redux actions in your reducers.
- **Sagas**: Generate sagas for handling side effects in your Redux application.
- **Selectors**: Generate selectors to access specific parts of your Redux state.

### New and Improved

The extension now supports generating boilerplate for `GET`, `POST`, `PUT`, and `DELETE` operations. Additionally, it can generate the full content for `constants.ts`, `saga.ts`, `reducer.ts`, and `selectors.ts` files.

### Example Snippets

#### Generate GET Saga

```json
{
  "Generate GET saga": {
    "prefix": "getSaga",
    "body": [
      "export function* get${1:Feature}Saga(action: Action<any, {}>) {",
      "  const url: string = `${WebService.WS_GET_${2:FEATURE}(action.params)}`;",
      "  try {",
      "    const resp = yield call(request.get, url);",
      "    yield put(get${1:Feature}SuccessAction(resp.data));",
      "  } catch (error) {",
      "    yield put(get${1:Feature}ErrorAction(error));",
      "  }",
      "}"
    ],
    "description": "Generate GET saga content for a given feature"
  }
}
```
