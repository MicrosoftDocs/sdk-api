---
UID: NF:commctrl.ImageList_DrawIndirect
title: ImageList_DrawIndirect function (commctrl.h)
description: Draws an image list image based on an IMAGELISTDRAWPARAMS structure.
helpviewer_keywords: ["ImageList_DrawIndirect","ImageList_DrawIndirect function [Windows Controls]","_win32_ImageList_DrawIndirect","_win32_ImageList_DrawIndirect_cpp","commctrl/ImageList_DrawIndirect","controls.ImageList_DrawIndirect","controls._win32_ImageList_DrawIndirect"]
old-location: controls\ImageList_DrawIndirect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_drawindirect.htm
ms.date: 12/05/2018
ms.keywords: ImageList_DrawIndirect, ImageList_DrawIndirect function [Windows Controls], _win32_ImageList_DrawIndirect, _win32_ImageList_DrawIndirect_cpp, commctrl/ImageList_DrawIndirect, controls.ImageList_DrawIndirect, controls._win32_ImageList_DrawIndirect
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
req.dll: Comctl32.dll (version 4.70 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_DrawIndirect
 - commctrl/ImageList_DrawIndirect
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
 - ImageList_DrawIndirect
---

# ImageList_DrawIndirect function


## -description

Draws an image list image based on an <a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imagelistdrawparams">IMAGELISTDRAWPARAMS</a> structure.

## -parameters

### -param pimldp

Type: <b><a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imagelistdrawparams">IMAGELISTDRAWPARAMS</a>*</b>

A pointer to an <a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imagelistdrawparams">IMAGELISTDRAWPARAMS</a> structure that contains information about the draw operation.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, and zero otherwise.