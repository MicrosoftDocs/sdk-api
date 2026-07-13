---
UID: NF:commctrl.ListView_GetToolTips
title: ListView_GetToolTips macro (commctrl.h)
description: Gets the tooltip control that the list-view control uses to display tooltips. You can use this macro or send the LVM_GETTOOLTIPS message explicitly.
helpviewer_keywords: ["ListView_GetToolTips","ListView_GetToolTips macro [Windows Controls]","_win32_ListView_GetToolTips","_win32_ListView_GetToolTips_cpp","commctrl/ListView_GetToolTips","controls.ListView_GetToolTips","controls._win32_ListView_GetToolTips"]
old-location: controls\ListView_GetToolTips.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gettooltips.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetToolTips, ListView_GetToolTips macro [Windows Controls], _win32_ListView_GetToolTips, _win32_ListView_GetToolTips_cpp, commctrl/ListView_GetToolTips, controls.ListView_GetToolTips, controls._win32_ListView_GetToolTips
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
 - ListView_GetToolTips
 - commctrl/ListView_GetToolTips
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
 - ListView_GetToolTips
---

# ListView_GetToolTips macro

## -syntax

```cpp
HWND ListView_GetToolTips(
   HWND hwndLV
);
```

## -returns

Type: **[HWND](/windows/desktop/winprog/windows-data-types)**

Returns the handle to the tooltip control.


## -description

Gets the tooltip control that the list-view control uses to display tooltips. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-gettooltips">LVM_GETTOOLTIPS</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-listview_settooltips">ListView_SetToolTips</a>
