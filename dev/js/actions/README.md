# Actions

Actions are just things that happen *(seriously, that's it)*.
- most actions are user events (clicked a button, submitted a form, etc...)
- can also be other events such as an API call returning data

### Actions are (usually) made up of two parts


**type** - describes the action that occurred
```
ADD_USER_BUTTON_CLICKED
```


**payload** - *(optional)* any extra data that is needed
```
{
    first: "Jean",
    last: "Patrick",
    age: 30,
    description: "He is working in New York."
}
```

## Actions vs. Action Creators

Action creators are functions that create objects, actions are the objects that get created.

**Action creator**
```
export default function () {
    return {
        first: "Jean",
        last: "Patrick",
        age: 30,
        description: "He is working in New York."
    }
}
```

**Action**
```
{
    first: "Jean",
    last: "Patrick",
    age: 30,
    description: "He is working in New York."
}
```

## What happens next?

All actions are automatically sent to **all** reducers. It is the reducers job to determine how to handle that action
(can also just ignore it).
