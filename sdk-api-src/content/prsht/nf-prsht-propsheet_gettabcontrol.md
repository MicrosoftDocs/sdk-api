---
UID: NF:prsht.PropSheet_GetTabControl
title: PropSheet_GetTabControl macro (prsht.h)
description: Retrieves the handle to the tab control of a property sheet. You can use this macro or send the PSM_GETTABCONTROL message explicitly.
helpviewer_keywords: ["PropSheet_GetTabControl","PropSheet_GetTabControl macro [Windows Controls]","_win32_PropSheet_GetTabControl","_win32_PropSheet_GetTabControl_cpp","controls.PropSheet_GetTabControl","controls._win32_PropSheet_GetTabControl","prsht/PropSheet_GetTabControl"]
old-location: controls\PropSheet_GetTabControl.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_gettabcontrol.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_GetTabControl, PropSheet_GetTabControl macro [Windows Controls], _win32_PropSheet_GetTabControl, _win32_PropSheet_GetTabControl_cpp, controls.PropSheet_GetTabControl, controls._win32_PropSheet_GetTabControl, prsht/PropSheet_GetTabControl
req.header: prsht.h
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
 - PropSheet_GetTabControl
 - prsht/PropSheet_GetTabControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PropSheet_GetTabControl
---

# PropSheet_GetTabControl macro

## -syntax

```cpp
HWND PropSheet_GetTabControl(
   HWND hDlg
);
```

## -returns

Type: **[HWND](/windows/desktop/winprog/windows-data-types)**

Returns the handle to the tab control.


## -description

Retrieves the handle to the tab control of a property sheet. You can use this macro or send the <a href="/windows/desktop/Controls/psm-gettabcontrol">PSM_GETTABCONTROL</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

## -remarks

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>
