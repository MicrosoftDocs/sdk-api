---
UID: NF:prsht.PropSheet_PressButton
title: PropSheet_PressButton macro
author: windows-sdk-content
description: Simulates the selection of a property sheet button. You can use this macro or send the PSM_PRESSBUTTON message explicitly.
old-location: controls\PropSheet_PressButton.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_pressbutton.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: PSBTN_APPLYNOW, PSBTN_BACK, PSBTN_CANCEL, PSBTN_FINISH, PSBTN_HELP, PSBTN_NEXT, PSBTN_OK, PropSheet_PressButton, PropSheet_PressButton macro [Windows Controls], _win32_PropSheet_PressButton, _win32_PropSheet_PressButton_cpp, controls.PropSheet_PressButton, controls._win32_PropSheet_PressButton, prsht/PropSheet_PressButton
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PropSheet_PressButton
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_PressButton macro


## -description


Simulates the selection of a property sheet button. You can use this macro or send the <a href="https://msdn.microsoft.com/82a55a29-d916-47ee-b0a0-f685a3a386d9">PSM_PRESSBUTTON</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


### -param iButton

Type: <b>int</b>

Index of the button to select. This parameter can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PSBTN_APPLYNOW"></a><a id="psbtn_applynow"></a><dl>
<dt><b>PSBTN_APPLYNOW</b></dt>
</dl>
</td>
<td width="60%">
Selects the Apply button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSBTN_BACK"></a><a id="psbtn_back"></a><dl>
<dt><b>PSBTN_BACK</b></dt>
</dl>
</td>
<td width="60%">
Selects the Back button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSBTN_CANCEL"></a><a id="psbtn_cancel"></a><dl>
<dt><b>PSBTN_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
Selects the Cancel button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSBTN_FINISH"></a><a id="psbtn_finish"></a><dl>
<dt><b>PSBTN_FINISH</b></dt>
</dl>
</td>
<td width="60%">
Selects the Finish button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSBTN_HELP"></a><a id="psbtn_help"></a><dl>
<dt><b>PSBTN_HELP</b></dt>
</dl>
</td>
<td width="60%">
Selects the Help button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSBTN_NEXT"></a><a id="psbtn_next"></a><dl>
<dt><b>PSBTN_NEXT</b></dt>
</dl>
</td>
<td width="60%">
Selects the Next button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSBTN_OK"></a><a id="psbtn_ok"></a><dl>
<dt><b>PSBTN_OK</b></dt>
</dl>
</td>
<td width="60%">
Selects the OK button.

</td>
</tr>
</table>
 

