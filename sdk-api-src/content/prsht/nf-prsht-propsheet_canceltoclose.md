---
UID: NF:prsht.PropSheet_CancelToClose
title: PropSheet_CancelToClose macro (prsht.h)
description: Used when changes made since the most recent PSN_APPLY notification cannot be canceled. You can also send a PSM_CANCELTOCLOSE message explicitly.
helpviewer_keywords: ["PropSheet_CancelToClose","PropSheet_CancelToClose macro [Windows Controls]","_win32_PropSheet_CancelToClose","_win32_PropSheet_CancelToClose_cpp","controls.PropSheet_CancelToClose","controls._win32_PropSheet_CancelToClose","prsht/PropSheet_CancelToClose"]
old-location: controls\PropSheet_CancelToClose.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_canceltoclose.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_CancelToClose, PropSheet_CancelToClose macro [Windows Controls], _win32_PropSheet_CancelToClose, _win32_PropSheet_CancelToClose_cpp, controls.PropSheet_CancelToClose, controls._win32_PropSheet_CancelToClose, prsht/PropSheet_CancelToClose
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
 - PropSheet_CancelToClose
 - prsht/PropSheet_CancelToClose
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
 - PropSheet_CancelToClose
---

# PropSheet_CancelToClose macro

## -syntax

```cpp
VOID PropSheet_CancelToClose(
   HWND hDlg
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

No return value.


## -description

Used when changes made since the most recent <a href="/windows/desktop/Controls/psn-apply">PSN_APPLY</a> notification cannot be canceled. You can also send a <a href="/windows/desktop/Controls/psm-canceltoclose">PSM_CANCELTOCLOSE</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

## -remarks

<a href="/windows/desktop/Controls/psm-canceltoclose">PSM_CANCELTOCLOSE</a> disables the <b>Cancel</b> button and changes the text of the <b>OK</b> button to "Close". You can use this macro or send the <b>PSM_CANCELTOCLOSE</b> message explicitly.

Most property sheets wait to perform irreversible changes until a <a href="/windows/desktop/Controls/psn-apply">PSN_APPLY</a> notification is received. However, in some circumstances, a property sheet may make irreversible changes outside the standard PSN_APPLY/<a href="/windows/desktop/Controls/psn-reset">PSN_RESET</a> sequence. One example is a property sheet that contains an <b>Edit</b> button that is used to display a subdialog box for editing a property. When the user clicks <b>OK</b> to submit the change, the property sheet page has several options:

<ul>
<li>It can record the changes but wait until it receives a <a href="/windows/desktop/Controls/psn-apply">PSN_APPLY</a> notification to apply them. This is the preferred approach.</li>
<li>It can apply the changes immediately after exiting the subdialog box, but remember the original settings. Those settings can be used to restore the original state if a <a href="/windows/desktop/Controls/psn-reset">PSN_RESET</a> notification is received.</li>
<li>It can apply the changes immediately and not attempt to restore the original settings when it receives a <a href="/windows/desktop/Controls/psn-reset">PSN_RESET</a> notification. This approach is not recommended, but may be necessary if the changes are too far-reaching for the other two options to be practical.</li>
</ul>
For the third option, applications should send a <a href="/windows/desktop/Controls/psm-canceltoclose">PSM_CANCELTOCLOSE</a> message to the property sheet. It indicates to the user that the changes made with the subdialog box cannot be reversed by clicking the <b>Cancel</b> button.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>
