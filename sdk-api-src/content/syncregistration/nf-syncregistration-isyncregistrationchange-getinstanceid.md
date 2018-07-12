---
UID: NF:syncregistration.ISyncRegistrationChange.GetInstanceId
title: ISyncRegistrationChange::GetInstanceId
author: windows-sdk-content
description: Gets the instance ID of the synchronization provider or synchronization provider configuration UI associated with the event.
old-location: winsync\isyncregistrationchange_getinstanceid.htm
old-project: winsync
ms.assetid: 2b2655f4-2a67-405d-93dc-dd8242992ce5
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetInstanceId, GetInstanceId method [Windows Sync], GetInstanceId method [Windows Sync],ISyncRegistrationChange interface, ISyncRegistrationChange interface [Windows Sync],GetInstanceId method, ISyncRegistrationChange.GetInstanceId, ISyncRegistrationChange::GetInstanceId, syncregistration/ISyncRegistrationChange::GetInstanceId, winsync.isyncregistrationchange_getinstanceid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SYNC_REGISTRATION_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncRegistrationChange.GetInstanceId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncRegistrationChange::GetInstanceId


## -description


Gets the instance ID of the synchronization provider or synchronization provider configuration UI associated with the event.


## -parameters




### -param pguidInstanceId [out]

The instance ID.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/45376bd2-1f5f-4f4c-9c4c-f5add9438d5c">ISyncRegistrationChange Interface</a>
 

 

