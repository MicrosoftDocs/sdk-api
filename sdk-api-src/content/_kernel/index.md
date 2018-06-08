---
UID: TP:kernel
ms.assetid: f7c71d77-9a5b-3320-80a1-302b75314d1e
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Kernel-Mode Driver Reference

## -description

Overview of the Kernel-Mode Driver Reference technology.

To develop Kernel-Mode Driver Reference, you need these headers:

 * [ntdef.h](..\ntdef\index.md)

For the programming guide, see [Kernel-Mode Driver Reference](/windows/desktop/kernel).

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
