---
UID: NF:commctrl.ImageList_DragLeave
title: ImageList_DragLeave function (commctrl.h)
description: Unlocks the specified window and hides the drag image, allowing the window to be updated.
helpviewer_keywords: ["ImageList_DragLeave","ImageList_DragLeave function [Windows Controls]","_win32_ImageList_DragLeave","_win32_ImageList_DragLeave_cpp","commctrl/ImageList_DragLeave","controls.ImageList_DragLeave","controls._win32_ImageList_DragLeave"]
old-location: controls\ImageList_DragLeave.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_dragleave.htm
ms.date: 12/05/2018
ms.keywords: ImageList_DragLeave, ImageList_DragLeave function [Windows Controls], _win32_ImageList_DragLeave, _win32_ImageList_DragLeave_cpp, commctrl/ImageList_DragLeave, controls.ImageList_DragLeave, controls._win32_ImageList_DragLeave
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
 - ImageList_DragLeave
 - commctrl/ImageList_DragLeave
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
 - ImageList_DragLeave
---

# ImageList_DragLeave function


## -description

Unlocks the specified window and hides the drag image, allowing the window to be updated.

## -parameters

### -param hwndLock

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that owns the drag image.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.