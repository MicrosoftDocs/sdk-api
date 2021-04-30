---
UID: NF:commctrl.ImageList_GetImageInfo
title: ImageList_GetImageInfo function (commctrl.h)
description: Retrieves information about an image.
helpviewer_keywords: ["ImageList_GetImageInfo","ImageList_GetImageInfo function [Windows Controls]","_win32_ImageList_GetImageInfo","_win32_ImageList_GetImageInfo_cpp","commctrl/ImageList_GetImageInfo","controls.ImageList_GetImageInfo","controls._win32_ImageList_GetImageInfo"]
old-location: controls\ImageList_GetImageInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_getimageinfo.htm
ms.date: 12/05/2018
ms.keywords: ImageList_GetImageInfo, ImageList_GetImageInfo function [Windows Controls], _win32_ImageList_GetImageInfo, _win32_ImageList_GetImageInfo_cpp, commctrl/ImageList_GetImageInfo, controls.ImageList_GetImageInfo, controls._win32_ImageList_GetImageInfo
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
 - ImageList_GetImageInfo
 - commctrl/ImageList_GetImageInfo
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
 - ImageList_GetImageInfo
---

# ImageList_GetImageInfo function


## -description

Retrieves information about an image.

## -parameters

### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list.

### -param i

Type: <b>int</b>

The index of the image.

### -param pImageInfo

Type: <b><a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imageinfo">IMAGEINFO</a>*</b>

A pointer to an <a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imageinfo">IMAGEINFO</a> structure that receives information about the image. The information in this structure can be used to directly manipulate the bitmaps for the image.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.

## -remarks

An application should not call <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> to destroy the bitmaps retrieved by <b>ImageList_GetImageInfo</b>. The system destroys the bitmaps when the application calls the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_destroy">ImageList_Destroy</a> function.