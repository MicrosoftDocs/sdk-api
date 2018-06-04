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

# ImmNotifyIME function


## -description


Notifies the IME about changes to the status of the input context.


## -parameters




### -param HIMC

TBD


### -param dwAction [in]

Notification code. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NI_CHANGECANDIDATELIST"></a><a id="ni_changecandidatelist"></a><dl>
<dt><b>NI_CHANGECANDIDATELIST</b></dt>
</dl>
</td>
<td width="60%">
An application changed the current selected candidate. The <i>dwIndex</i> parameter specifies an index of a candidate list to be selected and <i>dwValue</i> is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_CLOSECANDIDATE"></a><a id="ni_closecandidate"></a><dl>
<dt><b>NI_CLOSECANDIDATE</b></dt>
</dl>
</td>
<td width="60%">
An application directs the IME to close a candidate list. The <i>dwIndex</i> parameter specifies an index of the list to close, and <i>dwValue</i> is not used. The IME sends a <a href="https://msdn.microsoft.com/d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b">IMN_CLOSECANDIDATE</a> command to the application if it closes the list.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_COMPOSITIONSTR"></a><a id="ni_compositionstr"></a><dl>
<dt><b>NI_COMPOSITIONSTR</b></dt>
</dl>
</td>
<td width="60%">
An application directs the IME to carry out an action on the composition string. The <i>dwIndex</i> parameter can be CPS_CANCEL, CPS_COMPLETE, CPS_CONVERT, or CPS_REVERT.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_IMEMENUSELECTED"></a><a id="ni_imemenuselected"></a><dl>
<dt><b>NI_IMEMENUSELECTED</b></dt>
</dl>
</td>
<td width="60%">
An application directs the IME to allow the application to handle the specified menu. The <i>dwIndex</i> parameter specifies the ID of the menu and <i>dwValue</i> is an application-defined value for that menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_OPENCANDIDATE"></a><a id="ni_opencandidate"></a><dl>
<dt><b>NI_OPENCANDIDATE</b></dt>
</dl>
</td>
<td width="60%">
An application directs the IME to open a candidate list. The <i>dwIndex</i> parameter specifies the index of the list to open, and <i>dwValue</i> is not used. The IME sends a <a href="https://msdn.microsoft.com/439ff125-2731-4eb1-8287-4ca8ace7d8ec">IMN_OPENCANDIDATE</a> command to the application if it opens the list.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_SELECTCANDIDATESTR"></a><a id="ni_selectcandidatestr"></a><dl>
<dt><b>NI_SELECTCANDIDATESTR</b></dt>
</dl>
</td>
<td width="60%">
An application has selected one of the candidates. The <i>dwIndex</i> parameter specifies an index of a candidate list to be selected. The <i>dwValue</i> parameter specifies an index of a candidate string in the selected candidate list.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_SETCANDIDATE_PAGESIZE"></a><a id="ni_setcandidate_pagesize"></a><dl>
<dt><b>NI_SETCANDIDATE_PAGESIZE</b></dt>
</dl>
</td>
<td width="60%">
The application changes the page size of a candidate list. The <i>dwIndex</i> parameter specifies the candidate list to be changed and must have a value in the range 0 to 3. The <i>dwValue</i> parameter specifies the new page size.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_SETCANDIDATE_PAGESTART"></a><a id="ni_setcandidate_pagestart"></a><dl>
<dt><b>NI_SETCANDIDATE_PAGESTART</b></dt>
</dl>
</td>
<td width="60%">
The application changes the page starting index of a candidate list. The <i>dwIndex</i> parameter specifies the candidate list to be changed and must have a value in the range 0 to 3. The <i>dwValue</i> parameter specifies the new page start index.

</td>
</tr>
</table>
 


### -param dwIndex [in]

Index of a candidate list. Alternatively, if <i>dwAction</i> is NI_COMPOSITIONSTR, this parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CPS_CANCEL"></a><a id="cps_cancel"></a><dl>
<dt><b>CPS_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
Clear the composition string and set the status to no composition string.

</td>
</tr>
<tr>
<td width="40%"><a id="CPS_COMPLETE"></a><a id="cps_complete"></a><dl>
<dt><b>CPS_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Set the composition string as the result string.

</td>
</tr>
<tr>
<td width="40%"><a id="CPS_CONVERT"></a><a id="cps_convert"></a><dl>
<dt><b>CPS_CONVERT</b></dt>
</dl>
</td>
<td width="60%">
Convert the composition string.

</td>
</tr>
<tr>
<td width="40%"><a id="CPS_REVERT"></a><a id="cps_revert"></a><dl>
<dt><b>CPS_REVERT</b></dt>
</dl>
</td>
<td width="60%">
Cancel the current composition string and set the composition string to be the unconverted string.

</td>
</tr>
</table>
 


### -param dwValue [in]

Index of a candidate string. The application can set this parameter or ignore it, depending on the value of the <i>dwAction</i> parameter.


#### - hIMC [in]

Handle to the input context.


## -returns



Returns nonzero if successful, or 0 otherwise.




## -see-also




<a href="https://msdn.microsoft.com/d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b">IMN_CLOSECANDIDATE</a>



<a href="https://msdn.microsoft.com/439ff125-2731-4eb1-8287-4ca8ace7d8ec">IMN_OPENCANDIDATE</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

