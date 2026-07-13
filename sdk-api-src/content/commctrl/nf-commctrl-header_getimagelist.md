---
UID: NF:commctrl.Header_GetImageList
title: Header_GetImageList macro (commctrl.h)
description: Gets the handle to the image list that has been set for an existing header control. You can use this macro or send the HDM_GETIMAGELIST message explicitly.
helpviewer_keywords: ["Header_GetImageList","Header_GetImageList macro [Windows Controls]","_win32_Header_GetImageList","_win32_Header_GetImageList_cpp","commctrl/Header_GetImageList","controls.Header_GetImageList","controls._win32_Header_GetImageList"]
old-location: controls\Header_GetImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getimagelist.htm
ms.date: 10/21/2024
ms.keywords: Header_GetImageList, Header_GetImageList macro [Windows Controls], _win32_Header_GetImageList, _win32_Header_GetImageList_cpp, commctrl/Header_GetImageList, controls.Header_GetImageList, controls._win32_Header_GetImageList
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Header_GetImageList
 - commctrl/Header_GetImageList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Header_GetImageList
---

# Header_GetImageList macro

## -syntax

```cpp
HIMAGELIST Header_GetImageList(
   HWND hwnd
);
```

## -returns

Type: **HIMAGELIST**

Returns the handle to the image list that is set for the header control.


## -description

Gets the handle to the image list that has been set for an existing header control. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-getimagelist">HDM_GETIMAGELIST</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control.
