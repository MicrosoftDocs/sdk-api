---
UID: NF:commctrl.ListView_GetOrigin
title: ListView_GetOrigin macro (commctrl.h)
description: Gets the current view origin for a list-view control. You can use this macro or send the LVM_GETORIGIN message explicitly.
helpviewer_keywords: ["ListView_GetOrigin","ListView_GetOrigin macro [Windows Controls]","_win32_ListView_GetOrigin","_win32_ListView_GetOrigin_cpp","commctrl/ListView_GetOrigin","controls.ListView_GetOrigin","controls._win32_ListView_GetOrigin"]
old-location: controls\ListView_GetOrigin.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getorigin.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetOrigin, ListView_GetOrigin macro [Windows Controls], _win32_ListView_GetOrigin, _win32_ListView_GetOrigin_cpp, commctrl/ListView_GetOrigin, controls.ListView_GetOrigin, controls._win32_ListView_GetOrigin
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
 - ListView_GetOrigin
 - commctrl/ListView_GetOrigin
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
 - ListView_GetOrigin
---

# ListView_GetOrigin macro

## -syntax

```cpp
BOOL ListView_GetOrigin(
   HWND    hwndLV,
   LPPOINT ppt
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> if the current view is list or report view.


## -description

Gets the current view origin for a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getorigin">LVM_GETORIGIN</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param ppt

Type: <b>LPPOINT</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the view origin.
