---
UID: NF:windowsx.Edit_SetTabStops
title: Edit_SetTabStops macro (windowsx.h)
description: Sets the tab stops in a multiline edit or rich edit control. When text is copied to the control, any tab character in the text causes space to be generated up to the next tab stop. You can use this macro or send the EM_SETTABSTOPS message explicitly.
helpviewer_keywords: ["Edit_SetTabStops","Edit_SetTabStops macro [Windows Controls]","_win32_Edit_SetTabStops","_win32_Edit_SetTabStops_cpp","controls.Edit_SetTabStops","controls._win32_Edit_SetTabStops","windowsx/Edit_SetTabStops"]
old-location: controls\Edit_SetTabStops.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_settabstops.htm
ms.date: 10/21/2024
ms.keywords: Edit_SetTabStops, Edit_SetTabStops macro [Windows Controls], _win32_Edit_SetTabStops, _win32_Edit_SetTabStops_cpp, controls.Edit_SetTabStops, controls._win32_Edit_SetTabStops, windowsx/Edit_SetTabStops
req.header: windowsx.h
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
 - Edit_SetTabStops
 - windowsx/Edit_SetTabStops
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - Edit_SetTabStops
---

# Edit_SetTabStops macro

## -syntax

```cpp
void Edit_SetTabStops(
   HWND hwndCtl,
   int  cTabs,
   int  *lpTabs
);
```


## -description

Sets the tab stops in a multiline edit or rich edit control. When text is copied to the control, any tab character in the text causes space to be generated up to the next tab stop. You can use this macro or send the <a href="/windows/desktop/Controls/em-settabstops">EM_SETTABSTOPS</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param cTabs

Type: <b>int</b>

The number of tab stops contained in the array. If this parameter is zero, the <i>lpTabs</i> parameter is ignored and default tab stops are set at every 32 dialog template units. If this parameter is 1, tab stops are set at every <i>n</i> dialog template units, where <i>n</i> is the distance pointed to by the <i>lpTabs</i> parameter. If this parameter is greater than 1, <i>lpTabs</i> is a pointer to an array of tab stops.

### -param lpTabs

Type: <b>int*</b>

A pointer to an array of unsigned integers specifying the tab stops, in dialog template units. If <i>cTabs</i> is 1, this parameter is a pointer to an unsigned integer containing the distance between all tab stops, in dialog template units.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-settabstops">EM_SETTABSTOPS</a>.
