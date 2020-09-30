---
UID: NF:commctrl.ImageList_GetBkColor
title: ImageList_GetBkColor function (commctrl.h)
description: Retrieves the current background color for an image list.
helpviewer_keywords: ["ImageList_GetBkColor","ImageList_GetBkColor function [Windows Controls]","_win32_ImageList_GetBkColor","_win32_ImageList_GetBkColor_cpp","commctrl/ImageList_GetBkColor","controls.ImageList_GetBkColor","controls._win32_ImageList_GetBkColor"]
old-location: controls\ImageList_GetBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_getbkcolor.htm
ms.date: 12/05/2018
ms.keywords: ImageList_GetBkColor, ImageList_GetBkColor function [Windows Controls], _win32_ImageList_GetBkColor, _win32_ImageList_GetBkColor_cpp, commctrl/ImageList_GetBkColor, controls.ImageList_GetBkColor, controls._win32_ImageList_GetBkColor
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
 - ImageList_GetBkColor
 - commctrl/ImageList_GetBkColor
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
 - ImageList_GetBkColor
---

# ImageList_GetBkColor function


## -description

Retrieves the current background color for an image list.

## -parameters

### -param himl [in]

Type: <b>HIMAGELIST</b>

A handle to the image list.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The return value is the background color.