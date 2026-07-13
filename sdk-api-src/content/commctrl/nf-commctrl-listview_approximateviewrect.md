---
UID: NF:commctrl.ListView_ApproximateViewRect
title: ListView_ApproximateViewRect macro (commctrl.h)
description: Calculates the approximate width and height required to display a given number of items. You can use this macro or send the LVM_APPROXIMATEVIEWRECT message explicitly.
helpviewer_keywords: ["ListView_ApproximateViewRect","ListView_ApproximateViewRect macro [Windows Controls]","_win32_ListView_ApproximateViewRect","_win32_ListView_ApproximateViewRect_cpp","commctrl/ListView_ApproximateViewRect","controls.ListView_ApproximateViewRect","controls._win32_ListView_ApproximateViewRect"]
old-location: controls\ListView_ApproximateViewRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_approximateviewrect.htm
ms.date: 10/21/2024
ms.keywords: ListView_ApproximateViewRect, ListView_ApproximateViewRect macro [Windows Controls], _win32_ListView_ApproximateViewRect, _win32_ListView_ApproximateViewRect_cpp, commctrl/ListView_ApproximateViewRect, controls.ListView_ApproximateViewRect, controls._win32_ListView_ApproximateViewRect
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
 - ListView_ApproximateViewRect
 - commctrl/ListView_ApproximateViewRect
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
 - ListView_ApproximateViewRect
---

# ListView_ApproximateViewRect macro

## -syntax

```cpp
DWORD ListView_ApproximateViewRect(
   HWND hwnd,
   int    iWidth,
   int    iHeight,
   int    iCount
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns a <b>DWORD</b> value that holds the approximate width (in the LOWORD) and height (in the HIWORD) needed to display the items, in pixels.


## -description

Calculates the approximate width and height required to display a given number of items. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-approximateviewrect">LVM_APPROXIMATEVIEWRECT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iWidth

Type: <b>int</b>

The proposed x-dimension of the control, in pixels. This parameter can be -1 to allow the message to use the current width value.

### -param iHeight

Type: <b>int</b>

The proposed y-dimension of the control, in pixels. This parameter can be -1 to allow the message to use the current height value.

### -param iCount

Type: <b>int</b>

The number of items to be displayed in the control. If this parameter is -1, the message uses the total number of items in the control.
