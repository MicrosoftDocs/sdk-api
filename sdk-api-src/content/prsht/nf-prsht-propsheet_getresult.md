---
UID: NF:prsht.PropSheet_GetResult
title: PropSheet_GetResult macro (prsht.h)
description: Used by modeless property sheets to retrieve the information returned to modal property sheets by PropertySheet. You can use this macro or sent the PSM_GETRESULT message explicitly.
helpviewer_keywords: ["PropSheet_GetResult","PropSheet_GetResult macro [Windows Controls]","_win32_PropSheet_GetResult","_win32_PropSheet_GetResult_cpp","controls.PropSheet_GetResult","controls._win32_PropSheet_GetResult","prsht/PropSheet_GetResult"]
old-location: controls\PropSheet_GetResult.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_getresult.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_GetResult, PropSheet_GetResult macro [Windows Controls], _win32_PropSheet_GetResult, _win32_PropSheet_GetResult_cpp, controls.PropSheet_GetResult, controls._win32_PropSheet_GetResult, prsht/PropSheet_GetResult
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
 - PropSheet_GetResult
 - prsht/PropSheet_GetResult
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
 - PropSheet_GetResult
---

# PropSheet_GetResult macro

## -syntax

```cpp
int PropSheet_GetResult(
   HWND hDlg
);
```

## -returns

Type: **int**

Returns a positive value if successful, or -1 otherwise. The following return values have a special meaning.

| Return code | Description |
|---|---|
| ID_PSREBOOTSYSTEM | A page sent a PSM_REBOOTSYSTEM message to the property sheet. The computer must be restarted for the user's changes to take effect. |
| ID_PSRESTARTWINDOWS | A page sent a PSM_RESTARTWINDOWS message to the property sheet. Windows must be restarted for the user's changes to take effect. |


## -description

Used by modeless property sheets to retrieve the information returned to modal property sheets by <a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a>. You can use this macro or sent the <a href="/windows/desktop/Controls/psm-getresult">PSM_GETRESULT</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet's dialog box.

## -remarks

To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The return value is identical to what <a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> would have returned had this been a modal property sheet.


<a href="/windows/desktop/Controls/common-control-versions">Version 5.80.</a> The <a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> return value carries different information for modal and modeless property sheets. In some cases, modeless property sheets may need the information they would have received from <b>PropertySheet</b> if they had been modal. In particular, they may need to know whether ID_PSREBOOTSYSTEM or ID_PSRESTARTWINDOWS would have been returned.

For a modeless property sheet, your message loop should use <a href="/windows/desktop/Controls/psm-isdialogmessage">PSM_ISDIALOGMESSAGE</a> to pass messages to the property sheet dialog box, and <a href="/windows/desktop/Controls/psm-getcurrentpagehwnd">PSM_GETCURRENTPAGEHWND</a> to determine when to destroy the dialog box. When the user clicks the <b>OK</b> or <b>Cancel</b> button, <b>PSM_GETCURRENTPAGEHWND</b> returns <b>NULL</b>. You can then retrieve the value that a modal property sheet would have received from <a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> by sending a <a href="/windows/desktop/Controls/psm-getresult">PSM_GETRESULT</a> message.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>
