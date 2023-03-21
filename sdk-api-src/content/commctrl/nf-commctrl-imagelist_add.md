---
UID: NF:commctrl.ImageList_Add
title: ImageList_Add function (commctrl.h)
description: Adds an image or images to an image list. (ImageList_Add)
helpviewer_keywords: ["ImageList_Add","ImageList_Add function [Windows Controls]","_win32_ImageList_Add","_win32_ImageList_Add_cpp","commctrl/ImageList_Add","controls.ImageList_Add","controls._win32_ImageList_Add"]
old-location: controls\ImageList_Add.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_add.htm
ms.date: 12/05/2018
ms.keywords: ImageList_Add, ImageList_Add function [Windows Controls], _win32_ImageList_Add, _win32_ImageList_Add_cpp, commctrl/ImageList_Add, controls.ImageList_Add, controls._win32_ImageList_Add
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
 - ImageList_Add
 - commctrl/ImageList_Add
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
 - ImageList_Add
---

# ImageList_Add function


## -description

Adds an image or images to an image list.

## -parameters

### -param himl [in]

Type: <b>HIMAGELIST</b>

A handle to the image list.

### -param hbmImage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

A handle to the bitmap that contains the image or images. The number of images is inferred from the width of the bitmap.

### -param hbmMask [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

A handle to the bitmap that contains the mask. If no mask is used with the image list, this parameter is ignored. This parameter can be <b>NULL</b>.

## -returns

Type: <b>int</b>

Returns the index of the first new image if successful, or -1 otherwise.

## -remarks

The <b>ImageList_Add</b> function copies the bitmap to an internal data structure. Be sure to use the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete 
				<i>hbmImage</i> and 
				<i>hbmMask</i> after the function returns.
