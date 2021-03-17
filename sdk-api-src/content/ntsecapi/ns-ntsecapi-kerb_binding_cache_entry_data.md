---
UID: NS:ntsecapi._KERB_BINDING_CACHE_ENTRY_DATA
title: KERB_BINDING_CACHE_ENTRY_DATA (ntsecapi.h)
description: Specifies the data for the binding cache entry.
helpviewer_keywords: ["*PKERB_BINDING_CACHE_ENTRY_DATA","DS_INET_ADDRESS","DS_NETBIOS_ADDRESS","KERB_BINDING_CACHE_ENTRY_DATA","KERB_BINDING_CACHE_ENTRY_DATA structure [Security]","KERB_NO_DC_FLAGS","PKERB_BINDING_CACHE_ENTRY_DATA","PKERB_BINDING_CACHE_ENTRY_DATA structure pointer [Security]","ntsecapi/KERB_BINDING_CACHE_ENTRY_DATA","ntsecapi/PKERB_BINDING_CACHE_ENTRY_DATA","security.kerb_binding_cache_entry_data"]
old-location: security\kerb_binding_cache_entry_data.htm
tech.root: security
ms.assetid: C5452477-B412-4E0C-B692-D79A47B8025A
ms.date: 12/05/2018
ms.keywords: '*PKERB_BINDING_CACHE_ENTRY_DATA, DS_INET_ADDRESS, DS_NETBIOS_ADDRESS, KERB_BINDING_CACHE_ENTRY_DATA, KERB_BINDING_CACHE_ENTRY_DATA structure [Security], KERB_NO_DC_FLAGS, PKERB_BINDING_CACHE_ENTRY_DATA, PKERB_BINDING_CACHE_ENTRY_DATA structure pointer [Security], ntsecapi/KERB_BINDING_CACHE_ENTRY_DATA, ntsecapi/PKERB_BINDING_CACHE_ENTRY_DATA, security.kerb_binding_cache_entry_data'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: KERB_BINDING_CACHE_ENTRY_DATA, *PKERB_BINDING_CACHE_ENTRY_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_BINDING_CACHE_ENTRY_DATA
 - ntsecapi/_KERB_BINDING_CACHE_ENTRY_DATA
 - PKERB_BINDING_CACHE_ENTRY_DATA
 - ntsecapi/PKERB_BINDING_CACHE_ENTRY_DATA
 - KERB_BINDING_CACHE_ENTRY_DATA
 - ntsecapi/KERB_BINDING_CACHE_ENTRY_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_BINDING_CACHE_ENTRY_DATA
---

# KERB_BINDING_CACHE_ENTRY_DATA structure


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

The domain controller flags that the caller provides. These flags are needed to pass to the <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function.

### -field DcFlags

The domain controller flags. These flags are returned from the <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function.

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

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that specifies the name of the KDC.