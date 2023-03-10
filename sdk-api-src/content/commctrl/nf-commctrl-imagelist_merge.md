---
UID: NF:commctrl.ImageList_Merge
title: ImageList_Merge function (commctrl.h)
description: Creates a new image by combining two existing images. The function also creates a new image list in which to store the image.
helpviewer_keywords: ["ImageList_Merge","ImageList_Merge function [Windows Controls]","_win32_ImageList_Merge","_win32_ImageList_Merge_cpp","commctrl/ImageList_Merge","controls.ImageList_Merge","controls._win32_ImageList_Merge"]
old-location: controls\ImageList_Merge.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_merge.htm
ms.date: 12/05/2018
ms.keywords: ImageList_Merge, ImageList_Merge function [Windows Controls], _win32_ImageList_Merge, _win32_ImageList_Merge_cpp, commctrl/ImageList_Merge, controls.ImageList_Merge, controls._win32_ImageList_Merge
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_Merge
 - commctrl/ImageList_Merge
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_Merge
---

# ImageList_Merge function


## -description

Creates a new image by combining two existing images. The function also creates a new image list in which to store the image.

## -parameters

### -param himl1

Type: <b>HIMAGELIST</b>

A handle to the first image list.

### -param i1

Type: <b>int</b>

The index of the first existing image.

### -param himl2

Type: <b>HIMAGELIST</b>

A handle to the second image list.

### -param i2

Type: <b>int</b>

The index of the second existing image.

### -param dx

Type: <b>int</b>

The x-offset of the second image relative to the first image.

### -param dy

Type: <b>int</b>

The y-offset of the second image relative to the first image.

## -returns

Type: <b>HIMAGELIST</b>

Returns the handle to the new image list if successful, or <b>NULL</b> otherwise.

## -remarks

The new image consists of the second existing image drawn transparently over the first. The mask for the new image is the result of performing a logical OR operation on the masks of the two existing images.

