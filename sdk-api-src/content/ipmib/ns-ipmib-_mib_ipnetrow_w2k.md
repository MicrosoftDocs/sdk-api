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

# _MIB_IPNETROW_W2K structure


## -description


The 
<b>MIB_IPNETROW</b> structure contains information for an Address Resolution Protocol (ARP) table entry for an IPv4 address.


## -struct-fields




### -field dwIndex

Type: <b>DWORD</b>

The index of the adapter.


### -field dwPhysAddrLen

Type: <b>DWORD</b>

The length, in bytes, of the physical address.


### -field bPhysAddr

Type: <b>BYTE[MAXLEN_PHYSADDR]</b>

The physical address.


### -field dwAddr

Type: <b>DWORD</b>

The IPv4 address.


### -field dwType

Type: <b>DWORD</b>

The type of ARP entry. 

This member can be one of the values from the <b>MIB_IPNET_TYPE</b> enumeration type defined in the <i>Ipmib.h</i> header file included in the Windows SDK released for Windows Vista and later. For use with versions of the earlier Platform SDK, this enumeration is not defined and the constants must be used. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIB_IPNET_TYPE_OTHER"></a><a id="mib_ipnet_type_other"></a><dl>
<dt><b>MIB_IPNET_TYPE_OTHER</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Other

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPNET_TYPE_INVALID"></a><a id="mib_ipnet_type_invalid"></a><dl>
<dt><b>MIB_IPNET_TYPE_INVALID</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
An invalid ARP type. This can indicate an unreachable or incomplete ARP entry.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPNET_TYPE_DYNAMIC"></a><a id="mib_ipnet_type_dynamic"></a><dl>
<dt><b>MIB_IPNET_TYPE_DYNAMIC</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
A dynamic ARP type.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPNET_TYPE_STATIC"></a><a id="mib_ipnet_type_static"></a><dl>
<dt><b>MIB_IPNET_TYPE_STATIC</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
A static ARP type.

</td>
</tr>
</table>
 


## -remarks



On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the <b>MIB_IPNETROW</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="_iphlp_createipnetentry">CreateIpNetEntry</a>



<a href="_iphlp_deleteipnetentry">DeleteIpNetEntry</a>



<a href="https://msdn.microsoft.com/1cac1c19-bc42-4aee-b9d0-d007b8798eeb">MIB_IPNETTABLE</a>



<a href="_iphlp_setipnetentry">SetIpNetEntry</a>
 

 

