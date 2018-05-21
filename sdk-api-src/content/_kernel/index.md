---
UID: TP:kernel
ms.assetid: f7c71d77-9a5b-3320-80a1-302b75314d1e
ms.author: windowsdriverdev
ms.date: 05/21/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Kernel



Overview of the Kernel technology.

To develop Kernel, you need these headers:

 * [ntdef.h](..\ntdef\index.md)



## Structures

| Title   | Description   |
| ---- |:---- |
| [_LIST_ENTRY structure](..\ntdef\ns-ntdef-_list_entry.md) | A LIST_ENTRY structure describes an entry in a doubly linked list or serves as the header for such a list. |
| [_LUID structure](..\ntdef\ns-ntdef-_luid.md) | The LUID structure is an opaque structure that specifies an identifier that is guaranteed to be unique on the local machine. For more information, see the reference page for LUID in the Microsoft Windows SDK documentation. |
| [_SINGLE_LIST_ENTRY structure](..\ntdef\ns-ntdef-_single_list_entry.md) | A SINGLE_LIST_ENTRY structure describes an entry in a singly linked list, or serves as the header for such a list. |
| [_STRING structure](..\ntdef\ns-ntdef-_string.md) | The ANSI_STRING structure defines a counted string used for ANSI strings. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [COMPARTMENT_ID enumeration](..\ntdef\ne-ntdef-compartment_id.md) | The COMPARTMENT_ID enumeration indicates the network routing compartment identifier. |

## Macros

| Title   | Description   |
| ---- |:---- |
| [FIELD_OFFSET macro](..\ntdef\nf-ntdef-field_offset.md) | The FIELD_OFFSET macro returns the byte offset of a named field in a known structure type. |
