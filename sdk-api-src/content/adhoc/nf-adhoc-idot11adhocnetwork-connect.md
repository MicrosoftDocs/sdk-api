---
UID: NF:adhoc.IDot11AdHocNetwork.Connect
title: IDot11AdHocNetwork::Connect
author: windows-sdk-content
description: Connects to a previously created wireless ad hoc network.
old-location: nwifi\idot11adhocnetwork_connect.htm
old-project: nativewifi
ms.assetid: 3272e0fe-0844-4e02-bd5f-a1e1c656074d
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: Connect, Connect method [NativeWIFI], Connect method [NativeWIFI],IDot11AdHocNetwork interface, IDot11AdHocNetwork interface [NativeWIFI],Connect method, IDot11AdHocNetwork.Connect, IDot11AdHocNetwork::Connect, adhoc/IDot11AdHocNetwork::Connect, nwifi.idot11adhocnetwork_connect
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocNetwork.Connect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocNetwork::Connect


## -description


Connects to a previously created wireless ad hoc network. Before an application can connect to a network, the network must have been created using <a href="https://msdn.microsoft.com/1d9930b3-7bc4-4015-b096-a21fe01f54f5">IDot11AdHocManager::CreateNetwork</a> and committed using <a href="https://msdn.microsoft.com/45beb340-1c19-4b91-8e5c-8849e690e988">IDot11AdHocManager::CommitCreatedNetwork</a>.


## -parameters




### -param Passphrase [in]

The password string used to authenticate the user or machine on the network.

The length of the password string depends on the security settings passed in the <i>pSecurity</i> parameter of the <a href="https://msdn.microsoft.com/1d9930b3-7bc4-4015-b096-a21fe01f54f5">CreateNetwork</a> call. The following table shows the password length associated with various security settings.

<table>
<tr>
<th>Security Settings</th>
<th>Password Length</th>
</tr>
<tr>
<td>Open-None</td>
<td>0</td>
</tr>
<tr>
<td>Open-WEP</td>
<td>5 or 13 characters; 10 or 26 hexadecimal digits</td>
</tr>
<tr>
<td>WPA2PSK</td>
<td>8 to 63 characters</td>
</tr>
</table>
 

For the enumerated values that correspond to the security settings pair above, see <a href="https://msdn.microsoft.com/6e28fb8f-a429-4b6c-a057-737bbadb0a95">DOT11_ADHOC_AUTH_ALGORITHM</a> and <a href="https://msdn.microsoft.com/2ea8173d-f528-4065-90ce-71a455a6b35f">DOT11_ADHOC_CIPHER_ALGORITHM</a>.


### -param GeographicalId [in]

The geographical location in which the network was created. For a list of possible values, see <a href="https://msdn.microsoft.com/6e424bd4-389c-4f51-9898-f60a8a818f89">Table of Geographical Locations</a>.


### -param fSaveProfile [in]

An optional parameter that specifies whether a wireless profile should  be saved. If <b>TRUE</b>, the profile is saved to the profile store. Once a profile is saved, the user can modify the profile using the <b>Manage Wireless Network</b> user interface. Profiles can also be modified using the <a href="https://msdn.microsoft.com/c1816d68-48b2-4d3d-a8c8-4a243a4b3f3b">Native Wifi Functions</a>.

Saving a profile modifies the network signature returned by <a href="https://msdn.microsoft.com/0a59a8bd-d2eb-48c6-8480-dc4dea335d22">IDot11AdHocNetwork::GetSignature</a>.


### -param fMakeSavedProfileUserSpecific [in]

An optional parameter that specifies whether the profile to be saved is an all-user profile.  If set to <b>TRUE</b>, the profile is specific to the current user. If set to <b>FALSE</b>, the profile is an all-user profile and can be used by any user logged into the machine. This parameter is ignored if <i>fSaveProfile</i> is <b>FALSE</b>.

By default, only members of the Administrators group can save an all-user profile. These security settings can be altered using the <a href="https://msdn.microsoft.com/6038e4bc-7f07-4148-ac34-e290c8c40e99">WlanSetSecuritySettings</a> function. Your application must be launched by a user with sufficient privileges for an all-user profile to be saved successfully.

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
 




## -remarks



This method is asynchronous. <b>Connect</b> returns S_OK immediately if the parameters passed to the method are valid. However, a return code of S_OK does not indicate that the connection was successful. You must register for notifications on the <a href="https://msdn.microsoft.com/54a45431-8036-4a3f-9558-467a1efab6bb">IDot11AdHocNetworkNotificationSink</a> interface to be notified of connection success or failure. The <a href="https://msdn.microsoft.com/795057bf-d97e-40b8-b242-5e3859ad3038">IDot11AdHocNetworkNotificationSink::OnStatusChange</a> method returns the connection status. For more information about registering for notifications, see <a href="https://msdn.microsoft.com/dcb93b9c-3292-4cbf-9d44-5367bdbd4878">IDot11AdHocManager</a>.




## -see-also




<a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a>



<a href="https://msdn.microsoft.com/e5c96776-6bb2-43b0-86b9-c3bc058d5d84">IDot11AdHocNetwork::Disconnect</a>
 

 

