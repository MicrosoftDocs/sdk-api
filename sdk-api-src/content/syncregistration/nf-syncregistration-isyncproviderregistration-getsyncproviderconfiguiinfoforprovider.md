---
UID: NF:syncregistration.ISyncProviderRegistration.GetSyncProviderConfigUIInfoforProvider
title: ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider
author: windows-sdk-content
description: Returns an ISyncProviderConfigUIInfo object for the specified synchronization provider instance ID.
old-location: winsync\isyncproviderregistration_getsyncproviderconfiguiinfoforprovider.htm
old-project: winsync
ms.assetid: 6ef774f8-0b97-44ee-8bb9-7adf2293cc23
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetSyncProviderConfigUIInfoforProvider, GetSyncProviderConfigUIInfoforProvider method [Windows Sync], GetSyncProviderConfigUIInfoforProvider method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],GetSyncProviderConfigUIInfoforProvider method, ISyncProviderRegistration.GetSyncProviderConfigUIInfoforProvider, ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider, syncregistration/ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider, winsync.isyncproviderregistration_getsyncproviderconfiguiinfoforprovider
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
 - ISyncProviderRegistration.GetSyncProviderConfigUIInfoforProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider


## -description


Returns an <a href="https://msdn.microsoft.com/b7c49533-d289-44b0-9a9e-cfa47af3a087">ISyncProviderConfigUIInfo</a> object for the specified synchronization provider instance ID.


## -parameters




### -param pguidProviderInstanceId [in]

The unique instance ID of the synchronization provider.


### -param ppProviderConfigUIInfo [out]

The configuration UI information object.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No configuration UI was specified for the synchronization provider.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to return the synchronization provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_REGISTRATION_NOTREGISTERED  </b></dt>
</dl>
</td>
<td width="60%">
The specified instance ID does not match a registered synchronization provider, or the requested configuration UI is not registered.

</td>
</tr>
</table>
 




## -remarks



This method is used to get and set the configuration UI properties for the specified  synchronization provider and to obtain the <b>ISyncProviderConfigUI</b> instance.

This method is used to obtain an <b>ISyncProviderConfigUIInfo</b> object when the instance ID is not known, but the instance ID of the  synchronization provider is known. The <a href="https://msdn.microsoft.com/472732d7-39bd-434c-80f3-9808eca9035c">GetSyncProviderConfigUIFromInstanceId</a> method should be used if you want to access an <b>ISyncProviderConfigUIInfo</b> object directly using the instance ID of an <b>ISyncProviderConfigUI</b>.




## -see-also




<a href="https://msdn.microsoft.com/27757aa1-a42d-4f66-99a8-bf66385fbec1">ISyncProviderConfigUI Interface</a>



<a href="https://msdn.microsoft.com/b7c49533-d289-44b0-9a9e-cfa47af3a087">ISyncProviderConfigUIInfo Interface</a>



<a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration Interface</a>
 

 

