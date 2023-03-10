---
UID: NF:commctrl.ImageList_Remove
title: ImageList_Remove function (commctrl.h)
description: Removes an image from an image list. (ImageList_Remove)
helpviewer_keywords: ["ImageList_Remove","ImageList_Remove function [Windows Controls]","_win32_ImageList_Remove","_win32_ImageList_Remove_cpp","commctrl/ImageList_Remove","controls.ImageList_Remove","controls._win32_ImageList_Remove"]
old-location: controls\ImageList_Remove.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_remove.htm
ms.date: 12/05/2018
ms.keywords: ImageList_Remove, ImageList_Remove function [Windows Controls], _win32_ImageList_Remove, _win32_ImageList_Remove_cpp, commctrl/ImageList_Remove, controls.ImageList_Remove, controls._win32_ImageList_Remove
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
 - ImageList_Remove
 - commctrl/ImageList_Remove
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
 - ImageList_Remove
---

# ImageList_Remove function


## -description

Removes an image from an image list.

## -parameters

### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list.

### -param i

Type: <b>int</b>

The index of the image to remove. If this parameter is -1, the function removes all images.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.

## -remarks

When an image is removed, the indexes of the remaining images are adjusted so that the image indexes always range from zero to one less than the number of images in the image list. For example, if you remove the image at index 0, then image 1 becomes image 0, image 2 becomes image 1, and so on.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_removeall">ImageList_RemoveAll</a>
