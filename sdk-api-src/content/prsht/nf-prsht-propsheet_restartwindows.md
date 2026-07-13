---
UID: NF:prsht.PropSheet_RestartWindows
title: PropSheet_RestartWindows macro (prsht.h)
description: Sends a PSM_RESTARTWINDOWS message indicating that Windows needs to be restarted for changes to take effect. You can use this macro or send the PSM_RESTARTWINDOWS message explicitly.
helpviewer_keywords: ["PropSheet_RestartWindows","PropSheet_RestartWindows macro [Windows Controls]","_win32_PropSheet_RestartWindows","_win32_PropSheet_RestartWindows_cpp","controls.PropSheet_RestartWindows","controls._win32_PropSheet_RestartWindows","prsht/PropSheet_RestartWindows"]
old-location: controls\PropSheet_RestartWindows.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_restartwindows.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_RestartWindows, PropSheet_RestartWindows macro [Windows Controls], _win32_PropSheet_RestartWindows, _win32_PropSheet_RestartWindows_cpp, controls.PropSheet_RestartWindows, controls._win32_PropSheet_RestartWindows, prsht/PropSheet_RestartWindows
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
 - PropSheet_RestartWindows
 - prsht/PropSheet_RestartWindows
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
 - PropSheet_RestartWindows
---

# PropSheet_RestartWindows macro

## -syntax

```cpp
VOID PropSheet_RestartWindows(
   HWND hDlg
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

No return value.


## -description

Sends a <a href="/windows/desktop/Controls/psm-restartwindows">PSM_RESTARTWINDOWS</a> message indicating that Windows needs to be restarted for changes to take effect. You can use this macro or send the <b>PSM_RESTARTWINDOWS</b> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

## -remarks

An application should send the <a href="/windows/desktop/Controls/psm-restartwindows">PSM_RESTARTWINDOWS</a> message only in response to the <a href="/windows/desktop/Controls/psn-apply">PSN_APPLY</a> or <a href="/windows/desktop/Controls/psn-killactive">PSN_KILLACTIVE</a> notification code.

The <a href="/windows/desktop/Controls/psm-restartwindows">PSM_RESTARTWINDOWS</a> message causes the <a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function to return the ID_PSRESTARTWINDOWS value, but only if the user clicks the <b>OK</b> button to close the property sheet. It is the application's responsibility to restart Windows, which can be done by using the <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> function.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>
