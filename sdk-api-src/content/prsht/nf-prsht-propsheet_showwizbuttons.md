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

# PropSheet_ShowWizButtons macro


## -description


Show or hide buttons in a wizard. You can use this macro or send the <a href="https://msdn.microsoft.com/669c4e51-cac1-40e1-8f23-afae0e41fc9b">PSM_SHOWWIZBUTTONS</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the wizard.


### -param dwFlag

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

One or more of the same values used in <i>dwFlag</i>. Here, they specify which property sheet buttons are to be shown or hidden. If a button value appears in this parameter but not in <i>dwFlag</i>, it indicates that the button should be hidden.


## -remarks



The following example code hides the <b>Back</b> button and shows the <b>Next</b> button. 
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>PropSheet_ShowWizButtons(hwnd,
                         PSWIZB_NEXT,
                         PSWIZB_BACK | PSWIZB_NEXT);</pre>
</td>
</tr>
</table></span></div>


