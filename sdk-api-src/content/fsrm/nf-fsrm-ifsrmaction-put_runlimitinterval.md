---
UID: NF:fsrm.IFsrmAction.put_RunLimitInterval
title: IFsrmAction::put_RunLimitInterval
author: windows-sdk-content
description: Retrieves or sets the interval that must expire before the action is run again.
old-location: fsrm\ifsrmaction_runlimitinterval.htm
old-project: Fsrm
ms.assetid: 3d5be77f-282f-479d-aa34-a8cb1c771951
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmAction interface [File Server Resource Manager],RunLimitInterval property, IFsrmAction.RunLimitInterval, IFsrmAction.put_RunLimitInterval, IFsrmAction::RunLimitInterval, IFsrmAction::get_RunLimitInterval, IFsrmAction::put_RunLimitInterval, RunLimitInterval property [File Server Resource Manager], RunLimitInterval property [File Server Resource Manager],IFsrmAction interface, fs.ifsrmaction_runlimitinterval, fsrm.ifsrmaction_runlimitinterval, fsrm/IFsrmAction::RunLimitInterval, fsrm/IFsrmAction::get_RunLimitInterval, fsrm/IFsrmAction::put_RunLimitInterval, put_RunLimitInterval
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmAction.RunLimitInterval
-	IFsrmAction.get_RunLimitInterval
-	IFsrmAction.put_RunLimitInterval
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmAction::put_RunLimitInterval


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
 

 

