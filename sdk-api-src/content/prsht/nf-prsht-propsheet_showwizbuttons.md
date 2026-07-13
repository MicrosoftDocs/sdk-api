---
UID: NF:prsht.PropSheet_ShowWizButtons
title: PropSheet_ShowWizButtons macro (prsht.h)
description: Show or hide buttons in a wizard. You can use this macro or send the PSM_SHOWWIZBUTTONS message explicitly.
helpviewer_keywords: ["PSWIZB_BACK","PSWIZB_CANCEL","PSWIZB_FINISH","PSWIZB_NEXT","PSWIZB_RESTORE","PSWIZB_SHOW","PropSheet_ShowWizButtons","PropSheet_ShowWizButtons macro [Windows Controls]","_shell_PropSheet_ShowWizButtons","_shell_PropSheet_ShowWizButtons_cpp","controls.PropSheet_ShowWizButtons","controls._shell_PropSheet_ShowWizButtons","prsht/PropSheet_ShowWizButtons"]
old-location: controls\PropSheet_ShowWizButtons.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_showwizbuttons.htm
ms.date: 10/21/2024
ms.keywords: PSWIZB_BACK, PSWIZB_CANCEL, PSWIZB_FINISH, PSWIZB_NEXT, PSWIZB_RESTORE, PSWIZB_SHOW, PropSheet_ShowWizButtons, PropSheet_ShowWizButtons macro [Windows Controls], _shell_PropSheet_ShowWizButtons, _shell_PropSheet_ShowWizButtons_cpp, controls.PropSheet_ShowWizButtons, controls._shell_PropSheet_ShowWizButtons, prsht/PropSheet_ShowWizButtons
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
 - PropSheet_ShowWizButtons
 - prsht/PropSheet_ShowWizButtons
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
 - PropSheet_ShowWizButtons
---

# PropSheet_ShowWizButtons macro

## -syntax

```cpp
VOID PropSheet_ShowWizButtons(
   HWND  hDlg,
   DWORD dwFlag,
   DWORD dwButton
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

This macro does not return a value.


## -description

Show or hide buttons in a wizard. You can use this macro or send the <a href="/windows/desktop/Controls/psm-showwizbuttons">PSM_SHOWWIZBUTTONS</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the wizard.

### -param dwFlag

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

One or more of the following values that specify which property sheet buttons are to be shown. If a button value is included in both this parameter and <i>dwButton</i> then it is shown.

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
<tr>
<td width="40%"><a id="PSWIZB_SHOW"></a><a id="pswizb_show"></a><dl>
<dt><b>PSWIZB_SHOW</b></dt>
</dl>
</td>
<td width="60%">
Set only this flag (defined as zero) to hide all buttons specified in <i>dwButton</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_RESTORE"></a><a id="pswizb_restore"></a><dl>
<dt><b>PSWIZB_RESTORE</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>

### -param dwButton

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

One or more of the same values used in <i>dwFlag</i>. Here, they specify which property sheet buttons are to be shown or hidden. If a button value appears in this parameter but not in <i>dwFlag</i>, it indicates that the button should be hidden.

## -remarks

The following example code hides the <b>Back</b> button and shows the <b>Next</b> button. 
	


```
PropSheet_ShowWizButtons(hwnd,
                         PSWIZB_NEXT,
                         PSWIZB_BACK | PSWIZB_NEXT);
```
