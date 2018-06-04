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

# _KERB_BINDING_CACHE_ENTRY_DATA structure


## -description


Specifies the data for the binding cache entry. You must have the <b>SeTcbPrivilege</b> privilege set.


## -struct-fields




### -field DiscoveryTime

The time elapsed to find the domain controller to bind to.


### -field RealmName

The 	name of the realm for which to obtain a binding handle.


### -field KdcAddress

The address of the Key Distribution Center (KDC) of the server to  which you want to bind.


### -field AddressType

The type of string that is contained in the <b>KdcAddress</b> member. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DS_INET_ADDRESS"></a><a id="ds_inet_address"></a><dl>
<dt><b>DS_INET_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The address is a string IP address of the domain controller, for example, "\\157.55.94.74").

</td>
</tr>
<tr>
<td width="40%"><a id="DS_NETBIOS_ADDRESS"></a><a id="ds_netbios_address"></a><dl>
<dt><b>DS_NETBIOS_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The address is a NetBIOS name of the domain controller, for example, "\\phoenix".

</td>
</tr>
</table>
 


### -field Flags

The domain controller flags that the caller provides. These flags are needed to pass to the <a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a> function.


### -field DcFlags

The domain controller flags. These flags are returned from the <a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a> function.


### -field CacheFlags

Flags that provide more information about the binding cache.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_NO_DC_FLAGS"></a><a id="kerb_no_dc_flags"></a><dl>
<dt><b>KERB_NO_DC_FLAGS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
No flags are found for the binding cache.

</td>
</tr>
</table>
 


### -field KdcName


<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> that specifies the name of the KDC.

