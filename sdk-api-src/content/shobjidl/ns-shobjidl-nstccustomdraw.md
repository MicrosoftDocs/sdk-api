---
UID: NS:shobjidl.NSTCCUSTOMDRAW
title: NSTCCUSTOMDRAW
author: windows-sdk-content
description: Custom draw structure used by INameSpaceTreeControlCustomDraw methods.
old-location: shell\NSTCCUSTOMDRAW.htm
tech.root: shell
ms.assetid: 95747075-4882-4c29-8653-941ac04db54b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: NSTCCUSTOMDRAW, NSTCCUSTOMDRAW structure [Windows Shell], _shell_NSTCCUSTOMDRAW, shell.NSTCCUSTOMDRAW, shobjidl/NSTCCUSTOMDRAW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl.h
api_name:
 - NSTCCUSTOMDRAW
product: Windows
targetos: Windows
req.typenames: NSTCCUSTOMDRAW
req.redist: 
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

The current item state. See <a href="https://msdn.microsoft.com/en-us/library/Bb775483(v=VS.85).aspx">NMCUSTOMDRAW</a> for more detail.


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

