---
UID: NF:prsht.PropSheet_SetButtonText
title: PropSheet_SetButtonText macro
author: windows-sdk-content
description: Sets the text of a button in an Aero wizard. You can use this macro or send the PSM_SETBUTTONTEXT message explicitly.
old-location: controls\PropSheet_SetButtonText.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setbuttontext.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: PSWIZB_BACK, PSWIZB_CANCEL, PSWIZB_FINISH, PSWIZB_NEXT, PropSheet_SetButtonText, PropSheet_SetButtonText macro [Windows Controls], _win32_PropSheet_SetButtonText, _win32_PropSheet_SetButtonText_cpp, controls.PropSheet_SetButtonText, controls._win32_PropSheet_SetButtonText, prsht/PropSheet_SetButtonText
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
 - PropSheet_SetButtonText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_SetButtonText macro


## -description


Sets the text of a button in an Aero wizard. You can use this macro or send the <a href="https://msdn.microsoft.com/30b7afd1-5094-430f-9c48-d87832d96050">PSM_SETBUTTONTEXT</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the wizard.


### -param dwButton

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

One of the following values specifying the button whose text is set.

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
 


### -param lpszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

The text to set.

