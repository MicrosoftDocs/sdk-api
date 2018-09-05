---
UID: NF:syncregistration.ISyncProviderRegistration.SetSyncProviderState
title: ISyncProviderRegistration::SetSyncProviderState
author: windows-sdk-content
description: Sets the state of the specified synchronization provider.
old-location: winsync\isyncproviderregistration_setsyncproviderstate.htm
old-project: winsync
ms.assetid: 441df857-0498-4c6f-b279-495f1138e9c7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISyncProviderRegistration interface [Windows Sync],SetSyncProviderState method, ISyncProviderRegistration.SetSyncProviderState, ISyncProviderRegistration::SetSyncProviderState, SetSyncProviderState, SetSyncProviderState method [Windows Sync], SetSyncProviderState method [Windows Sync],ISyncProviderRegistration interface, syncregistration/ISyncProviderRegistration::SetSyncProviderState, winsync.isyncproviderregistration_setsyncproviderstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncregistration.h
req.include-header: 
req.redist: 
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
 - ISyncProviderRegistration.SetSyncProviderState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncProviderRegistration::SetSyncProviderState


## -description


Sets the state of the specified synchronization provider.


## -parameters




### -param pguidInstanceId [in]

The unique instance ID of the synchronization provider.


### -param dwStateFlagsMask [in]

A synchronization provider state flag that can be used to mask (preserve or remove) the existing state. If this parameter is set to zero, all synchronization provider states will be enumerated. See the <i>dwStateFlags</i> parameter description for a list of flags.


### -param dwStateFlags [in]

One of the following flags that represent the synchronization provider state.

<ul>
<li><b>SYNC_PROVIDER_STATE_ENABLED</b>  ((DWORD)0x00000001)The provider is enabled and available for synchronization.

</li>
<li><b>SYNC_PROVIDER_STATE_DIRTY</b>  ((DWORD)0x00000002)The active provider has been updated and has new data to synchronize.

</li>
</ul>
If this parameter is set to zero, all synchronization provider states will be enumerated.


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
A synchronization provider with the specified instance ID was not registered.

</td>
</tr>
</table>
 




## -remarks



To get the synchronization provider state, call the <a href="https://msdn.microsoft.com/4e2e2e17-e435-4def-9aee-9109e0e06a8c">GetSyncProviderState</a> method.




## -see-also




<a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration Interface</a>
 

 

