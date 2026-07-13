---
UID: NF:commctrl.ListView_SetWorkAreas
title: ListView_SetWorkAreas macro (commctrl.h)
description: Sets the working areas within a list-view control. You can use this macro or send the LVM_SETWORKAREAS message explicitly.
helpviewer_keywords: ["ListView_SetWorkAreas","ListView_SetWorkAreas macro [Windows Controls]","_win32_ListView_SetWorkAreas","_win32_ListView_SetWorkAreas_cpp","commctrl/ListView_SetWorkAreas","controls.ListView_SetWorkAreas","controls._win32_ListView_SetWorkAreas"]
old-location: controls\ListView_SetWorkAreas.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setworkareas.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetWorkAreas, ListView_SetWorkAreas macro [Windows Controls], _win32_ListView_SetWorkAreas, _win32_ListView_SetWorkAreas_cpp, commctrl/ListView_SetWorkAreas, controls.ListView_SetWorkAreas, controls._win32_ListView_SetWorkAreas
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
 - ListView_SetWorkAreas
 - commctrl/ListView_SetWorkAreas
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
 - ListView_SetWorkAreas
---

# ListView_SetWorkAreas macro

## -syntax

```cpp
void ListView_SetWorkAreas(
   HWND   hwnd,
   INT    nWorkAreas,
   LPRECT prc
);
```


## -description

Sets the working areas within a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setworkareas">LVM_SETWORKAREAS</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control.

### -param nWorkAreas

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

The number of <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures in the array at <i>prc</i>. The maximum number of working areas allowed is defined by the <b>LV_MAX_WORKAREAS</b> value.

### -param prc

Type: <b>LPRECT</b>

A pointer to an array of <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures that contain the new working areas of the list-view control. Values in these structures are in client coordinates. If this parameter is <b>NULL</b>, the working area will be set to the client area of the control. <i>nWorkAreas</i> specifies the number of structures in this array.

## -see-also

<a href="/windows/desktop/Controls/using-list-view-controls">Using List-View Controls</a>
