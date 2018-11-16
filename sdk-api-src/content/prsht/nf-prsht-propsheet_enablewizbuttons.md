---
UID: NF:prsht.PropSheet_EnableWizButtons
title: PropSheet_EnableWizButtons macro
author: windows-sdk-content
description: Enables or disables buttons in an Aero wizard. You can use this macro or send the PSM_ENABLEWIZBUTTONS message explicitly.
old-location: controls\PropSheet_EnableWizButtons.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_enablewizbuttons.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PSWIZB_BACK, PSWIZB_CANCEL, PSWIZB_FINISH, PSWIZB_NEXT, PropSheet_EnableWizButtons, PropSheet_EnableWizButtons macro [Windows Controls], _win32_PropSheet_EnableWizButtons, _win32_PropSheet_EnableWizButtons_cpp, controls.PropSheet_EnableWizButtons, controls._win32_PropSheet_EnableWizButtons, prsht/PropSheet_EnableWizButtons
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PropSheet_EnableWizButtons
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- prsht.h
: 
- PropSheet_EnableWizButtons
: 
---

# PropSheet_EnableWizButtons macro


## -description


Enables or disables buttons in an Aero wizard. You can use this macro or send the <a href="https://msdn.microsoft.com/9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4">PSM_ENABLEWIZBUTTONS</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the wizard.


### -param dwState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

One or more of the same values used in <i>dwState</i>, specifying which buttons are affected by this call. If a button value appears in this parameter but not in <i>dwState</i>, the button is disabled.


## -remarks



The following example code enables the <b>Back</b> button and disables the <b>Next</b> button.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>PropSheet_EnableWizButtons(hwnd,
                         PSWIZB_NEXT,
                         PSWIZB_BACK | PSWIZB_NEXT);</pre>
</td>
</tr>
</table></span></div>


