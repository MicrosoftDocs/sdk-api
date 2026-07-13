---
UID: NF:commctrl.ListView_GetWorkAreas
title: ListView_GetWorkAreas macro (commctrl.h)
description: Gets the working areas from a list-view control. You can use this macro, or send the LVM_GETWORKAREAS message explicitly.
helpviewer_keywords: ["ListView_GetWorkAreas","ListView_GetWorkAreas macro [Windows Controls]","_win32_ListView_GetWorkAreas","_win32_ListView_GetWorkAreas_cpp","commctrl/ListView_GetWorkAreas","controls.ListView_GetWorkAreas","controls._win32_ListView_GetWorkAreas"]
old-location: controls\ListView_GetWorkAreas.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getworkareas.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetWorkAreas, ListView_GetWorkAreas macro [Windows Controls], _win32_ListView_GetWorkAreas, _win32_ListView_GetWorkAreas_cpp, commctrl/ListView_GetWorkAreas, controls.ListView_GetWorkAreas, controls._win32_ListView_GetWorkAreas
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
 - ListView_GetWorkAreas
 - commctrl/ListView_GetWorkAreas
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
 - ListView_GetWorkAreas
---

# ListView_GetWorkAreas macro

## -syntax

```cpp
void ListView_GetWorkAreas(
   HWND   hwnd,
   INT    nWorkAreas,
   LPRECT prc
);
```


## -description

Gets the working areas from a list-view control. You can use this macro, or send the <a href="/windows/desktop/Controls/lvm-getworkareas">LVM_GETWORKAREAS</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param nWorkAreas

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

The number of <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures in the array at <i>prc</i>.

### -param prc

Type: <b>LPRECT</b>

A pointer to an array of <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures that receive the working areas of the list-view control. Values in these structures are in client coordinates. <i>nWorkAreas</i>  specifies the number of structures in this array.

## -see-also

<a href="/windows/desktop/Controls/using-list-view-controls">Using List-View Controls</a>
