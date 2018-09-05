---
UID: NS:ntsecapi._KERB_ADD_BINDING_CACHE_ENTRY_REQUEST
title: "_KERB_ADD_BINDING_CACHE_ENTRY_REQUEST"
author: windows-sdk-content
description: Specifies a message to add a binding cache entry.
old-location: security\kerb_add_binding_cache_entry_request.htm
old-project: SecAuthN
ms.assetid: 2EFB8F01-0665-4031-B02A-8ECB5B9C7C21
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST, DS_INET_ADDRESS, DS_NETBIOS_ADDRESS, KERB_ADD_BINDING_CACHE_ENTRY_REQUEST, KERB_ADD_BINDING_CACHE_ENTRY_REQUEST structure [Security], PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST, PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST structure pointer [Security], _KERB_ADD_BINDING_CACHE_ENTRY_REQUEST, ntsecapi/KERB_ADD_BINDING_CACHE_ENTRY_REQUEST, ntsecapi/PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST, security.kerb_add_binding_cache_entry_request"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: KERB_ADD_BINDING_CACHE_ENTRY_REQUEST, *PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_ADD_BINDING_CACHE_ENTRY_REQUEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _KERB_ADD_BINDING_CACHE_ENTRY_REQUEST structure


## -description


Specifies a message to add a binding cache entry. You must have the <b>SeTcbPrivilege</b> privilege set.


## -struct-fields




### -field MessageType

A 
						value of the <a href="https://msdn.microsoft.com/8ad183d2-3fe8-4f52-bfa4-16f2a711f0c3">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration that lists the types of messages that can be sent to the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> authentication package by calling 
the <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> function. This member must be set to <b>KerbAddBindingCacheEntryMessage</b>.


### -field RealmName

The 	name of the realm of the domain controller.


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
 

