---
UID: NF:prsht.PropSheet_EnableWizButtons
title: PropSheet_EnableWizButtons macro (prsht.h)
description: Enables or disables buttons in an Aero wizard. You can use this macro or send the PSM_ENABLEWIZBUTTONS message explicitly.
helpviewer_keywords: ["PSWIZB_BACK","PSWIZB_CANCEL","PSWIZB_FINISH","PSWIZB_NEXT","PropSheet_EnableWizButtons","PropSheet_EnableWizButtons macro [Windows Controls]","_win32_PropSheet_EnableWizButtons","_win32_PropSheet_EnableWizButtons_cpp","controls.PropSheet_EnableWizButtons","controls._win32_PropSheet_EnableWizButtons","prsht/PropSheet_EnableWizButtons"]
old-location: controls\PropSheet_EnableWizButtons.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_enablewizbuttons.htm
ms.date: 10/21/2024
ms.keywords: PSWIZB_BACK, PSWIZB_CANCEL, PSWIZB_FINISH, PSWIZB_NEXT, PropSheet_EnableWizButtons, PropSheet_EnableWizButtons macro [Windows Controls], _win32_PropSheet_EnableWizButtons, _win32_PropSheet_EnableWizButtons_cpp, controls.PropSheet_EnableWizButtons, controls._win32_PropSheet_EnableWizButtons, prsht/PropSheet_EnableWizButtons
req.header: prsht.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - PropSheet_EnableWizButtons
 - prsht/PropSheet_EnableWizButtons
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
 - PropSheet_EnableWizButtons
---

# PropSheet_EnableWizButtons macro

## -syntax

```cpp
VOID PropSheet_EnableWizButtons(
   HWND  hDlg,
   DWORD dwState,
   DWORD dwMask
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

No meaningful return value.


## -description

Enables or disables buttons in an Aero wizard. You can use this macro or send the <a href="/windows/desktop/Controls/psm-enablewizbuttons">PSM_ENABLEWIZBUTTONS</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the wizard.

### -param dwState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

One or more of the following values that specify which property sheet buttons are to be enabled. If a button value is included in both this parameter and <i>dwMask</i>, it is enabled.

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
0x0001. The <b>Back</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_NEXT"></a><a id="pswizb_next"></a><dl>
<dt><b>PSWIZB_NEXT</b></dt>
</dl>
</td>
<td width="60%">
0x0002. The <b>Next</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_FINISH"></a><a id="pswizb_finish"></a><dl>
<dt><b>PSWIZB_FINISH</b></dt>
</dl>
</td>
<td width="60%">
0x0004. The <b>Finish</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_CANCEL"></a><a id="pswizb_cancel"></a><dl>
<dt><b>PSWIZB_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
0x0010. The <b>Cancel</b> button.

</td>
</tr>
</table>

### -param dwMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

One or more of the same values used in <i>dwState</i>, specifying which buttons are affected by this call. If a button value appears in this parameter but not in <i>dwState</i>, the button is disabled.

## -remarks

The following example code enables the <b>Back</b> button and disables the <b>Next</b> button.


```
PropSheet_EnableWizButtons(hwnd,
                         PSWIZB_NEXT,
                         PSWIZB_BACK | PSWIZB_NEXT);
```
