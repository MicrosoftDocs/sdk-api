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

# IFsrmAction::get_RunLimitInterval


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets the interval that must expire before the action is run again.

This property is read/write.


## -parameters


## -remarks



This property specifies the interval that should occur before the action is run again. For example, if the 
    interval has expired since the action last ran, the server will run the action again in response to an event; 
    otherwise, the server cannot run the action again.

You can specify the interval as follows.

<table>
<tr>
<th>Interval</th>
<th>Description</th>
</tr>
<tr>
<td>
–1

</td>
<td>
Use the global run-time limit. For a description, see the 
       <a href="https://msdn.microsoft.com/4cd4d583-2906-4ba0-b113-c21db143dec2">IFsrmSetting::SetActionRunLimitInterval</a> 
       method.

</td>
</tr>
<tr>
<td>
0

</td>
<td>
Run the action for each quota or file screen event.

</td>
</tr>
<tr>
<td>
&gt;0

</td>
<td>
If an event occurs during this interval, do not run the action again. The interval timer starts when the 
       action begins. When the interval expires, the timer is reset.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a>
 

 

