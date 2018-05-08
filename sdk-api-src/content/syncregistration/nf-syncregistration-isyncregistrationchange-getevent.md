---
UID: NF:syncregistration.ISyncRegistrationChange.GetEvent
title: ISyncRegistrationChange::GetEvent
author: windows-driver-content
description: Gets the next pending registration event.
old-location: winsync\isyncregistrationchange_getevent.htm
old-project: winsync
ms.assetid: 7c96c6ad-13ca-4e00-8e6e-61898206001f
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetEvent, GetEvent method [Windows Sync], GetEvent method [Windows Sync],ISyncRegistrationChange interface, ISyncRegistrationChange interface [Windows Sync],GetEvent method, ISyncRegistrationChange.GetEvent, ISyncRegistrationChange::GetEvent, syncregistration/ISyncRegistrationChange::GetEvent, winsync.isyncregistrationchange_getevent
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SYNC_REGISTRATION_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncregistration.h
api_name:
-	ISyncRegistrationChange.GetEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncRegistrationChange::GetEvent


## -description


Gets the next pending registration event.


## -parameters




### -param psreEvent [out]

The registration event.


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
 

 

