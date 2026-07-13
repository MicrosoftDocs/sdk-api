---
UID: NF:prsht.PropSheet_SetWizButtons
title: PropSheet_SetWizButtons macro (prsht.h)
description: Enables or disables the Back, Next, and Finish buttons in a wizard by posting a PSM_SETWIZBUTTONS message. You can use this macro or send the PSM_SETWIZBUTTONS message explicitly.
helpviewer_keywords: ["PSWIZB_BACK","PSWIZB_DISABLEDFINISH","PSWIZB_FINISH","PSWIZB_NEXT","PropSheet_SetWizButtons","PropSheet_SetWizButtons macro [Windows Controls]","_win32_PropSheet_SetWizButtons","_win32_PropSheet_SetWizButtons_cpp","controls.PropSheet_SetWizButtons","controls._win32_PropSheet_SetWizButtons","prsht/PropSheet_SetWizButtons"]
old-location: controls\PropSheet_SetWizButtons.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setwizbuttons.htm
ms.date: 10/21/2024
ms.keywords: PSWIZB_BACK, PSWIZB_DISABLEDFINISH, PSWIZB_FINISH, PSWIZB_NEXT, PropSheet_SetWizButtons, PropSheet_SetWizButtons macro [Windows Controls], _win32_PropSheet_SetWizButtons, _win32_PropSheet_SetWizButtons_cpp, controls.PropSheet_SetWizButtons, controls._win32_PropSheet_SetWizButtons, prsht/PropSheet_SetWizButtons
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
 - PropSheet_SetWizButtons
 - prsht/PropSheet_SetWizButtons
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
 - PropSheet_SetWizButtons
---

# PropSheet_SetWizButtons macro

## -syntax

```cpp
VOID PropSheet_SetWizButtons(
   HWND  hDlg,
   DWORD dwFlags
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

No return value.


## -description

Enables or disables the Back, Next, and Finish buttons in a wizard by posting a <a href="/windows/desktop/Controls/psm-setwizbuttons">PSM_SETWIZBUTTONS</a> message. You can use this macro or send the <b>PSM_SETWIZBUTTONS</b> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

### -param dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A value that specifies which wizard buttons are enabled. You can combine one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_BACK"></a><a id="pswizb_back"></a><dl>
<dt><b>PSWIZB_BACK</b></dt>
</dl>
</td>
<td width="60%">
Enable the Back button. If this flag is not set, the Back button is displayed as disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_DISABLEDFINISH"></a><a id="pswizb_disabledfinish"></a><dl>
<dt><b>PSWIZB_DISABLEDFINISH</b></dt>
</dl>
</td>
<td width="60%">
Display a disabled Finish button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_FINISH"></a><a id="pswizb_finish"></a><dl>
<dt><b>PSWIZB_FINISH</b></dt>
</dl>
</td>
<td width="60%">
Display an enabled Finish button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_NEXT"></a><a id="pswizb_next"></a><dl>
<dt><b>PSWIZB_NEXT</b></dt>
</dl>
</td>
<td width="60%">
Enable the Next button. If this flag is not set, the Next button is displayed as disabled.

</td>
</tr>
</table>

## -remarks

This macro uses <a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a> to send the <a href="/windows/desktop/Controls/psm-setwizbuttons">PSM_SETWIZBUTTONS</a> message. If your notification handler calls <b>PropSheet_SetWizButtons</b>, do nothing that will affect window focus until after the handler returns. For example, if you call <a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a> immediately after calling <b>PropSheet_SetWizButtons</b>, the message box will receive focus. Since messages sent with <b>PostMessage</b> are not delivered until they reach the head of the message queue, the <b>PSM_SETWIZBUTTONS</b> message will not be delivered until after the wizard has lost focus to the message box. As a result, the property sheet will not be able to properly set the focus for the buttons.

Wizards display either three or four buttons below each page. This message is used to specify which buttons are enabled. Wizards normally display Back, Cancel, and either a Next or Finish button. You typically enable only the Next button for the welcome page, Next and Back for interior pages, and Back and Finish for the completion page. The Cancel button is always enabled. Normally, setting PSWIZB_FINISH or PSWIZB_DISABLEDFINISH replaces the Next button with a Finish button. To display Next and Finish buttons simultaneously, set the PSH_WIZARDHASFINISH FLAG in the <b>dwFlags</b> member of the wizard's <a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PROPSHEETHEADER</a> structure when you create the wizard. Every page will then display all four buttons.
