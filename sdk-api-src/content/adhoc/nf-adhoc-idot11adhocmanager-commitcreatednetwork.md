---
UID: NF:adhoc.IDot11AdHocManager.CommitCreatedNetwork
title: IDot11AdHocManager::CommitCreatedNetwork (adhoc.h)
author: windows-sdk-content
description: Initializes a created network and optionally commits the network's profile to the profile store.
old-location: nwifi\idot11adhocmanager_commitcreatednetwork.htm
tech.root: NativeWiFi
ms.assetid: 45beb340-1c19-4b91-8e5c-8849e690e988
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CommitCreatedNetwork, CommitCreatedNetwork method [NativeWIFI], CommitCreatedNetwork method [NativeWIFI],IDot11AdHocManager interface, IDot11AdHocManager interface [NativeWIFI],CommitCreatedNetwork method, IDot11AdHocManager.CommitCreatedNetwork, IDot11AdHocManager::CommitCreatedNetwork, adhoc/IDot11AdHocManager::CommitCreatedNetwork, nwifi.idot11adhocmanager_commitcreatednetwork
ms.topic: method
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocManager.CommitCreatedNetwork
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDot11AdHocManager::CommitCreatedNetwork


## -description


Initializes a created network and optionally commits the network's profile to the profile store. The network must be created using <a href="https://msdn.microsoft.com/1d9930b3-7bc4-4015-b096-a21fe01f54f5">CreateNetwork</a> before calling <b>CommitCreatedNetwork</b>.


## -parameters




### -param pIAdHoc [in]

A pointer to a <a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a> interface that specifies the network to be initialized and committed.


### -param fSaveProfile [in]

An optional parameter that specifies whether a wireless profile should  be saved. If <b>TRUE</b>, the profile is saved to the profile store. Once a profile has been saved, the user can modify the profile using the <b>Manage Wireless Network</b> user interface. Profiles can also be modified using the <a href="https://msdn.microsoft.com/c1816d68-48b2-4d3d-a8c8-4a243a4b3f3b">Native Wifi Functions</a>.

Saving a profile modifies the network signature returned by <a href="https://msdn.microsoft.com/0a59a8bd-d2eb-48c6-8480-dc4dea335d22">IDot11AdHocNetwork::GetSignature</a>.


### -param fMakeSavedProfileUserSpecific [in]

An optional parameter that specifies whether the profile to be saved is an all-user profile.  If set to <b>TRUE</b>, the profile is specific to the current user. If set to <b>FALSE</b>, the profile is an all-user profile and can be used by any user logged into the machine. This parameter is ignored if <i>fSaveProfile</i> is <b>FALSE</b>. 

By default, only members of the Administrators group can persist an all-user profile. These security settings can be altered using the <a href="https://msdn.microsoft.com/6038e4bc-7f07-4148-ac34-e290c8c40e99">WlanSetSecuritySettings</a> function. Your application must be launched by a user with sufficient privileges for an all-user profile to be persisted successfully.

If your application is running in a Remote Desktop window, you can only save an all-user profile. User-specific profiles cannot be saved from an application running remotely.


## -returns



Possible return values include, but are not limited to, the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A specified interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/dcb93b9c-3292-4cbf-9d44-5367bdbd4878">IDot11AdHocManager</a>



<a href="https://msdn.microsoft.com/1d9930b3-7bc4-4015-b096-a21fe01f54f5">IDot11AdHocManager::CreateNetwork</a>
 

 

