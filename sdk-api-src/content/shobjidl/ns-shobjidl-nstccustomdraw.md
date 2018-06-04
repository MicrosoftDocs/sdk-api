---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NSTCCUSTOMDRAW structure


## -description


Custom draw structure used by <a href="https://msdn.microsoft.com/eac7c7c2-87f0-4af1-bf2f-f4fef5ddd92e">INameSpaceTreeControlCustomDraw</a> methods.


## -struct-fields




### -field psi

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to a Shell item.


### -field uItemState

Type: <b>UINT</b>

The current item state. See <a href="https://msdn.microsoft.com/c8a990a9-fb39-46e7-a5d2-fc817ff46e1b">NMCUSTOMDRAW</a> for more detail.


### -field nstcis

Type: <b><a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a></b>

The state of a tree item. See <a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a>.


### -field pszText

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string that contains the item text, if the structure specifies item attributes.


### -field iImage

Type: <b>int</b>

The index in the tree-view control's image list.


### -field himl

Type: <b>HIMAGELIST</b>

A handle to an image list.


### -field iLevel

Type: <b>int</b>

The zero-based level of the item being drawn.


### -field iIndent

Type: <b>int</b>

A tree-level indent.

