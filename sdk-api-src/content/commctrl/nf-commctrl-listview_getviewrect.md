---
UID: NF:commctrl.ListView_GetViewRect
title: ListView_GetViewRect macro (commctrl.h)
description: Gets the bounding rectangle of all items in the list-view control. The list view must be in icon or small icon view. You can use this macro or send the LVM_GETVIEWRECT message explicitly.
helpviewer_keywords: ["ListView_GetViewRect","ListView_GetViewRect macro [Windows Controls]","_win32_ListView_GetViewRect","_win32_ListView_GetViewRect_cpp","commctrl/ListView_GetViewRect","controls.ListView_GetViewRect","controls._win32_ListView_GetViewRect"]
old-location: controls\ListView_GetViewRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getviewrect.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetViewRect, ListView_GetViewRect macro [Windows Controls], _win32_ListView_GetViewRect, _win32_ListView_GetViewRect_cpp, commctrl/ListView_GetViewRect, controls.ListView_GetViewRect, controls._win32_ListView_GetViewRect
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
 - ListView_GetViewRect
 - commctrl/ListView_GetViewRect
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
 - ListView_GetViewRect
---

# ListView_GetViewRect macro

## -syntax

```cpp
BOOL ListView_GetViewRect(
   HWND hwnd,
   RECT *prc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Gets the bounding rectangle of all items in the list-view control. The list view must be in icon or small icon view. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getviewrect">LVM_GETVIEWRECT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param prc

Type: <b><a href="/windows/win32/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-rect">RECT</a> structure that receives the bounding rectangle. All coordinates are relative to the visible area of the list-view control.
