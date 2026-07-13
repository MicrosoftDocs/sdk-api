---
UID: NF:commctrl.TabCtrl_SetItemExtra
title: TabCtrl_SetItemExtra macro (commctrl.h)
description: Sets the number of bytes per tab reserved for application-defined data in a tab control. You can use this macro or send the TCM_SETITEMEXTRA message explicitly.
helpviewer_keywords: ["TabCtrl_SetItemExtra","TabCtrl_SetItemExtra macro [Windows Controls]","_win32_TabCtrl_SetItemExtra","_win32_TabCtrl_SetItemExtra_cpp","commctrl/TabCtrl_SetItemExtra","controls.TabCtrl_SetItemExtra","controls._win32_TabCtrl_SetItemExtra"]
old-location: controls\TabCtrl_SetItemExtra.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setitemextra.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_SetItemExtra, TabCtrl_SetItemExtra macro [Windows Controls], _win32_TabCtrl_SetItemExtra, _win32_TabCtrl_SetItemExtra_cpp, commctrl/TabCtrl_SetItemExtra, controls.TabCtrl_SetItemExtra, controls._win32_TabCtrl_SetItemExtra
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
 - TabCtrl_SetItemExtra
 - commctrl/TabCtrl_SetItemExtra
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
 - TabCtrl_SetItemExtra
---

# TabCtrl_SetItemExtra macro

## -syntax

```cpp
BOOL TabCtrl_SetItemExtra(
   HWND hwndTC,
   int  cb
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sets the number of bytes per tab reserved for application-defined data in a tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-setitemextra">TCM_SETITEMEXTRA</a> message explicitly.

## -parameters

### -param hwndTC

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param cb

Type: <b>int</b>

Number of extra bytes.

## -remarks

By default, the number of extra bytes is four. An application that changes the number of extra bytes cannot use the <a href="/windows/desktop/api/commctrl/ns-commctrl-tcitema">TCITEM</a> structure to retrieve and set the application-defined data for a tab. Instead, you must define a new structure that consists of the <a href="/windows/desktop/api/commctrl/ns-commctrl-tcitemheadera">TCITEMHEADER</a> structure followed by application-defined members. 

An application should only change the number of extra bytes when a tab control does not contain any tabs.
