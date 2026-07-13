---
UID: NF:commctrl.TabCtrl_AdjustRect
title: TabCtrl_AdjustRect macro (commctrl.h)
description: Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a specified display area. You can use this macro or send the TCM_ADJUSTRECT message explicitly.
helpviewer_keywords: ["TabCtrl_AdjustRect","TabCtrl_AdjustRect macro [Windows Controls]","_win32_TabCtrl_AdjustRect","_win32_TabCtrl_AdjustRect_cpp","commctrl/TabCtrl_AdjustRect","controls.TabCtrl_AdjustRect","controls._win32_TabCtrl_AdjustRect"]
old-location: controls\TabCtrl_AdjustRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_adjustrect.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_AdjustRect, TabCtrl_AdjustRect macro [Windows Controls], _win32_TabCtrl_AdjustRect, _win32_TabCtrl_AdjustRect_cpp, commctrl/TabCtrl_AdjustRect, controls.TabCtrl_AdjustRect, controls._win32_TabCtrl_AdjustRect
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
 - TabCtrl_AdjustRect
 - commctrl/TabCtrl_AdjustRect
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
 - TabCtrl_AdjustRect
---

# TabCtrl_AdjustRect macro

## -syntax

```cpp
int TabCtrl_AdjustRect(
   HWND hwnd,
   BOOL bLarger,
   RECT *prc
);
```

## -returns

Type: **int**

No return value.


## -description

Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a specified display area. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-adjustrect">TCM_ADJUSTRECT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param bLarger

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Operation to perform. If this parameter is <b>TRUE</b>, 
					<i>prc</i> specifies a display rectangle and receives the corresponding window rectangle. If this parameter is <b>FALSE</b>, 
					<i>prc</i> specifies a window rectangle and receives the corresponding display area.

### -param prc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the given rectangle and receives the calculated rectangle.

## -remarks

This message applies only to tab controls that are at the top. It does not apply to tab controls that are on the sides or bottom.
