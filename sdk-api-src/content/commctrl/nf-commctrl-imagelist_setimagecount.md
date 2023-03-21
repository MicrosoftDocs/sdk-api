---
UID: NF:commctrl.ImageList_SetImageCount
title: ImageList_SetImageCount function (commctrl.h)
description: Resizes an existing image list. (ImageList_SetImageCount)
helpviewer_keywords: ["ImageList_SetImageCount","ImageList_SetImageCount function [Windows Controls]","_win32_ImageList_SetImageCount","_win32_ImageList_SetImageCount_cpp","commctrl/ImageList_SetImageCount","controls.ImageList_SetImageCount","controls._win32_ImageList_SetImageCount"]
old-location: controls\ImageList_SetImageCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_setimagecount.htm
ms.date: 12/05/2018
ms.keywords: ImageList_SetImageCount, ImageList_SetImageCount function [Windows Controls], _win32_ImageList_SetImageCount, _win32_ImageList_SetImageCount_cpp, commctrl/ImageList_SetImageCount, controls.ImageList_SetImageCount, controls._win32_ImageList_SetImageCount
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
 - ImageList_SetImageCount
 - commctrl/ImageList_SetImageCount
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
 - ImageList_SetImageCount
---

# ImageList_SetImageCount function


## -description

Resizes an existing image list.

## -parameters

### -param himl [in]

Type: <b>HIMAGELIST</b>

A handle to the image list that will be resized.

### -param uNewCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value specifying the new size of the image list.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.

## -remarks

If an application expands an image list with this function, it must add new images by using the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_replace">ImageList_Replace</a> function. If your application does not add valid images at the new indexes, draw operations that use the new indexes will be unpredictable. 

If you decrease the size of an image list by using this function, the truncated images are freed.
