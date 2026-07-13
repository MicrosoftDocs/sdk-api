---
UID: NF:commctrl.MonthCal_GetMinReqRect
title: MonthCal_GetMinReqRect macro (commctrl.h)
description: Retrieves the minimum size required to display a full month in a month calendar control. Size information is presented in the form of a RECT structure. You can use this macro or send the MCM_GETMINREQRECT message explicitly.
helpviewer_keywords: ["MonthCal_GetMinReqRect","MonthCal_GetMinReqRect macro [Windows Controls]","_win32_MonthCal_GetMinReqRect","_win32_MonthCal_GetMinReqRect_cpp","commctrl/MonthCal_GetMinReqRect","controls.MonthCal_GetMinReqRect","controls._win32_MonthCal_GetMinReqRect"]
old-location: controls\MonthCal_GetMinReqRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getminreqrect.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_GetMinReqRect, MonthCal_GetMinReqRect macro [Windows Controls], _win32_MonthCal_GetMinReqRect, _win32_MonthCal_GetMinReqRect_cpp, commctrl/MonthCal_GetMinReqRect, controls.MonthCal_GetMinReqRect, controls._win32_MonthCal_GetMinReqRect
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
 - MonthCal_GetMinReqRect
 - commctrl/MonthCal_GetMinReqRect
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
 - MonthCal_GetMinReqRect
---

# MonthCal_GetMinReqRect macro

## -syntax

```cpp
BOOL MonthCal_GetMinReqRect(
   HWND   hmc,
   LPRECT prc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero and <b>MonthCal_GetMinReqRect</b> receives the applicable bounding information if successful. Otherwise, the return is zero.

## -description

Retrieves the minimum size required to display a full month in a month calendar control. Size information is presented in the form of a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getminreqrect">MCM_GETMINREQRECT</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param prc

Type: <b>LPRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that will receive bounding rectangle information. This parameter must be a valid address and cannot be <b>NULL</b>.

## -remarks

The minimum required window size for a month calendar control depends on the currently selected font, control styles, system metrics, and regional settings. When an application changes anything that affects the minimum window size, or processes a <a href="/windows/desktop/winmsg/wm-settingchange">WM_SETTINGCHANGE</a> message, it should call <b>MonthCal_GetMinReqRect</b> to determine the new minimum size.

<div class="alert"><b>Note</b>  The rectangle returned by <b>MonthCal_GetMinReqRect</b> does not include the width of the "Today" string, if it is present. If the <a href="/windows/desktop/Controls/month-calendar-control-styles">MCS_NOTODAY</a> style is not set, your application should also retrieve the rectangle that defines the "Today" string width by calling the <a href="/windows/desktop/api/commctrl/nf-commctrl-monthcal_getmaxtodaywidth">MonthCal_GetMaxTodayWidth</a> macro. Use the larger of the two rectangles to ensure that the "Today" string is not clipped.</div>
<div> </div>
The <b>top</b> and <b>left</b> members of <i>prc</i> will always be zero. The <b>right</b> and <b>bottom</b> members represent the minimum <i>cx</i> and <i>cy</i> required for the control.
