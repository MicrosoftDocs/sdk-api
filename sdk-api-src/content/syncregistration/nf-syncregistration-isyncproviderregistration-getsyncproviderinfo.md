---
UID: NF:syncregistration.ISyncProviderRegistration.GetSyncProviderInfo
title: ISyncProviderRegistration::GetSyncProviderInfo
author: windows-sdk-content
description: Returns an ISyncProviderInfo object for the specific synchronization provider instance ID.
old-location: winsync\isyncproviderregistration_getsyncproviderinfo.htm
old-project: winsync
ms.assetid: 894d2314-2210-4a16-a7e6-1ee74638c035
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetSyncProviderInfo, GetSyncProviderInfo method [Windows Sync], GetSyncProviderInfo method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],GetSyncProviderInfo method, ISyncProviderRegistration.GetSyncProviderInfo, ISyncProviderRegistration::GetSyncProviderInfo, syncregistration/ISyncProviderRegistration::GetSyncProviderInfo, winsync.isyncproviderregistration_getsyncproviderinfo
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
 - ISyncProviderRegistration.GetSyncProviderInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncProviderRegistration::GetSyncProviderInfo


## -description


Returns an <a href="https://msdn.microsoft.com/fe50e34c-6499-4c1e-b891-7b4f797510f2">ISyncProviderInfo</a> object for the specific synchronization provider instance ID.


## -parameters




### -param pguidInstanceId [in]

The unique instance ID of the synchronization provider.


### -param ppProviderInfo [out]

The synchronization provider information object.


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
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_REGISTRATION_NOTREGISTERED  </b></dt>
</dl>
</td>
<td width="60%">
The specified instance ID does not match a registered synchronization provider.

</td>
</tr>
</table>
 




## -remarks



By calling the <a href="https://msdn.microsoft.com/74b70f31-0934-4599-9515-e94b6622d440">GetSyncProvider</a>
method of the <b>ISyncProviderInfo</b> object that is returned by this method,  you can get and set the properties of the synchronization provider, and  obtain the synchronization provider's <a href="https://msdn.microsoft.com/53970f17-2857-4624-8594-069cceb93b1e">IRegisteredSyncProvider</a> instance.




## -see-also




<a href="https://msdn.microsoft.com/53970f17-2857-4624-8594-069cceb93b1e">IRegisteredSyncProvider Interface</a>



<a href="https://msdn.microsoft.com/fe50e34c-6499-4c1e-b891-7b4f797510f2">ISyncProviderInfo Interface</a>



<a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration Interface</a>
 

 

