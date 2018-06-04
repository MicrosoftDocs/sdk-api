---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PropSheet_PressButton macro


## -description


Simulates the selection of a property sheet button. You can use this macro or send the <a href="https://msdn.microsoft.com/82a55a29-d916-47ee-b0a0-f685a3a386d9">PSM_PRESSBUTTON</a> message explicitly.


## -parameters




### -param hDlg

TBD


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
 


#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.

