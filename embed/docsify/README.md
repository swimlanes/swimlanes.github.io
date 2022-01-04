# Test docsify plugin

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla in varius velit. Proin ut est ex. Proin a nisl eu nulla mollis hendrerit. Morbi non tincidunt urna. Cras sapien mi, tincidunt aliquam lacus eget, molestie pulvinar dui. Proin ut est ac arcu convallis finibus lobortis vel ipsum. Nam lobortis pulvinar magna, at pulvinar augue condimentum vel. Quisque rutrum aliquet nisl sit amet tempus. Aliquam consequat sapien tempor consectetur pharetra. Donec nec ornare nulla.

## Markdown

```swimlanes-io
title: Swimlanes.io full syntax overview


_: **1. Messages**
One -> Two: Simple
Two ->> Three: Open arrow 
Three -x Four: Lost message

Three <-> Four: Bi-directional
Two -> Two: To self

Two -> One: Actors can be
One <- Two: in any order

Two -> Three: Regular
Two <-- Three: Dashed 
Two => Three: Bold

One -> Four: Markdown support for messages: *Italic*, **Bold**, ~~strike through~~ and `inline code`. + {fab-font-awesome} Icons
```

Vivamus a molestie enim, et maximus neque. Donec convallis arcu lorem, ut semper lacus suscipit quis. Aenean luctus ornare aliquam. Proin cursus turpis at mi blandit pulvinar. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Morbi fringilla dui id euismod accumsan. Pellentesque tortor eros, tincidunt non velit id, efficitur tristique lorem. Cras consectetur, justo ut faucibus suscipit, enim urna efficitur nisl, eget tempus sem felis sed augue. Donec tellus turpis, suscipit id condimentum eget, porta non lorem. Pellentesque eget laoreet quam, ac blandit velit.

## swimlanes-io tag

<swimlanes-io>  
title: Swimlanes.io full syntax overview


_: **1. Messages**
One -> Two: Simple
Two ->> Three: Open arrow 
Three -x Four: Lost message

Three <-> Four: Bi-directional
Two -> Two: To self

Two -> One: Actors can be
One <- Two: in any order

Two -> Three: Regular
Two <-- Three: Dashed 
Two => Three: Bold

One -> Four: Markdown support for messages: *Italic*, **Bold**, ~~strike through~~ and `inline code`. + {fab-font-awesome} Icons



note: Add sequence numbers to messages with the _**autonumber**_ statement

// Uncomment next line for automatic message numbering
// autonumber



_: **2. Notes**

note:
Simple text formatting; **bold**, *italic*, ~~strike through~~ and `inline code`. + {fab-font-awesome} Icons

1. Ordered
2. list


* Unordered
* list

[link](http://www.swimlanes.io)

```
{
  code block..
}
```

Two -> Three: A note is closed by a following element

note: A note spans the length of the previoues message by default

note One, Three: Specify the start and end actor to change the width of a note
```
note [start[,end]]: text
```

_: **3. Sections**

if: Define conditional flows with _**if**_
  Two -> Three: Message
else: Optional alternative flow with _**else**_
  Two -> One: Message
else
  One <-> Four: Section lables are optional
  if: Sections can be nested one level
  end
    note One, Three: Sections are closed with the _**end**_ statement
end

group: _**group**_ can be used instead of _**if**_ for simple grouping

end


_: **4. Dividers**

_: thin

-: regular

--: dashed

=: bold

-: Markdown support for dividers: *Italic*, **Bold**, ~~strike through~~ and `inline code`. + {fab-font-awesome} Icons

_: **5. {fab-font-awesome fa-lg} Icons**

note: {far-bolt fa-lg} Font Awesome icons are supported using:
```
{fa$-icon}
```
Where **$** is:
- **b** for brand
- **s** for solid
- **r** for regular
- **l** for light
- **d** for duotone

See [Font Awesome overview](/gallery/font-awesome) for more details and [fontawesome.com](https://fontawesome.com/v5.10.1/icons?d=gallery) for a full list of available icons.

_: **6. Delay**

...: {fas-spinner} Indicate a delay in the flow



_: **7. Order**
note: Change the order of the actors with the _**order**_ statement

```
order: first [,second[,third ...]]
```

// Uncomment next line for re-ordering
// order: Three, Two
</swimlanes-io>