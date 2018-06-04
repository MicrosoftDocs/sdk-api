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

# WlanDisconnect function


## -description


The <b>WlanDisconnect</b> function  disconnects an interface from its current network.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pInterfaceGuid [in]

The GUID of the interface to be disconnected.


### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value may be one of the following return codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>hClientHandle</i> is <b>NULL</b> or invalid,  <i>pInterfaceGuid</i> is <b>NULL</b>, or <i>pReserved</i> is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle <i>hClientHandle</i>  was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Various error codes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate memory for the query results.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient permissions. 

</td>
</tr>
</table>
 




## -remarks



When the connection was established using <a href="https://msdn.microsoft.com/24ab2024-e786-454f-860f-cf2431f001bb">WlanConnect</a>, a profile was specified by the <b>strProfile</b> member of the <a href="https://msdn.microsoft.com/e0321447-b89a-4f4e-929e-eb6db76f7283">WLAN_CONNECTION_PARAMETERS</a> structure pointed to by  <i>pConnectionParameters</i>. If that profile was an all-user profile, the <b>WlanDisconnect</b>  caller must have execute access on the profile. Otherwise, the <b>WlanDisconnect</b> call will fail with return value ERROR_ACCESS_DENIED. The permissions on an all-user profile are established when the profile is created or saved using <a href="https://msdn.microsoft.com/3f8dca2e-6fe5-4c7d-a135-a33c61ba3dd5">WlanSetProfile</a> or <a href="https://msdn.microsoft.com/e409fd30-eddd-4cc7-acb7-35af6ef51a10">WlanSaveTemporaryProfile</a>.

To perform a disconnection operation at the command line, use the <b>netsh wlan disconnect</b> command. For more information, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=120964">Netsh Commands for Wireless Local Area Network (wlan)</a>. 

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b><b>WlanDisconnect</b> has the side effect of modifying the profile associated with the disconnected network. A network profile becomes an on-demand profile after a <b>WlanDisconnect</b> call. The Wireless Zero Configuration service will not connect automatically to a network with an on-demand profile when the network is in range. Do not call <b>WlanDisconnect</b> before calling <a href="https://msdn.microsoft.com/24ab2024-e786-454f-860f-cf2431f001bb">WlanConnect</a> unless you want to change a profile to an on-demand profile. When you call <b>WlanConnect</b> to establish a network connection, any existing network connection is dropped automatically.






## -see-also




<a href="https://msdn.microsoft.com/24ab2024-e786-454f-860f-cf2431f001bb">WlanConnect</a>
 

 

