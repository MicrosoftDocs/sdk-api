---
UID: NF:syncregistration.ISyncProviderRegistration.GetSyncProviderFromInstanceId
title: ISyncProviderRegistration::GetSyncProviderFromInstanceId
author: windows-driver-content
description: Returns an initialized and instantiated IRegisteredSyncProvider object for the specific unique instance ID.
old-location: winsync\isyncproviderregistration_getsyncproviderfrominstanceid.htm
old-project: winsync
ms.assetid: ed204998-9e9a-4bac-b178-b4137be87ff4
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetSyncProviderFromInstanceId, GetSyncProviderFromInstanceId method [Windows Sync], GetSyncProviderFromInstanceId method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],GetSyncProviderFromInstanceId method, ISyncProviderRegistration.GetSyncProviderFromInstanceId, ISyncProviderRegistration::GetSyncProviderFromInstanceId, syncregistration/ISyncProviderRegistration::GetSyncProviderFromInstanceId, winsync.isyncproviderregistration_getsyncproviderfrominstanceid
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
-	ISyncProviderRegistration.GetSyncProviderFromInstanceId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncProviderRegistration::GetSyncProviderFromInstanceId


## -description


Returns an initialized and instantiated  <a href="https://msdn.microsoft.com/53970f17-2857-4624-8594-069cceb93b1e">IRegisteredSyncProvider</a> object for the specific unique instance ID.


## -parameters




### -param pguidInstanceId [in]

The unique instance ID of the <b>IRegisteredSyncProvider</b> object.


### -param dwClsContext [in]

The context in which the code that manages the newly created object will run. The only context supported is <b>CLSCTX_INPROC_SERVER</b>.


### -param ppSyncProvider [out]

The initialized and instantiated synchronization provider object.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The instance ID is <b>GUID_NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to create the synchronization provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The synchronization provider’s CLSID is not registered with the requested context or the provider has not had its DLL registered.

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



<div class="alert"><b>Note</b>  The caller of this method should not explicitly call <b>IRegisteredSyncProvider::Init</b>
        on the <b>IRegisteredSyncProvider</b> object that is returned, as this method will do this on the caller's behalf. The caller should call <b>QueryInterface</b> on the <b>IRegisteredSyncProvider</b> object that is returned to obtain an <a href="https://msdn.microsoft.com/0664267f-90ba-4123-bfe5-7cf748b78c10">ISyncProvider</a> interface to pass to the synchronization session.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/53970f17-2857-4624-8594-069cceb93b1e">IRegisteredSyncProvider Interface</a>



<a href="https://msdn.microsoft.com/0664267f-90ba-4123-bfe5-7cf748b78c10">ISyncProvider Interface</a>



<a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration Interface</a>
 

 

