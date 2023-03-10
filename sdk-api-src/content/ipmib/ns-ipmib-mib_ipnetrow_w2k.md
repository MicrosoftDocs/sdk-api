---
UID: NS:ipmib._MIB_IPNETROW_W2K
title: MIB_IPNETROW_W2K (ipmib.h)
description: MIB_IPNETROW_W2K (ipmib.h) contains information for an Address Resolution Protocol (ARP) table entry for an IPv4 address.
helpviewer_keywords: ["*PMIB_IPNETROW","*PMIB_IPNETROW_W2K","MIB_IPNETROW","MIB_IPNETROW structure [MIB]","MIB_IPNETROW_W2K","MIB_IPNET_TYPE_DYNAMIC","MIB_IPNET_TYPE_INVALID","MIB_IPNET_TYPE_OTHER","MIB_IPNET_TYPE_STATIC","PMIB_IPNETROW","PMIB_IPNETROW structure pointer [MIB]","_mpr_mib_ipnetrow","ipmib/MIB_IPNETROW","ipmib/PMIB_IPNETROW","iprtrmib/MIB_IPNETROW","iprtrmib/PMIB_IPNETROW","mib.mib_ipnetrow","rras.mib_ipnetrow"]
old-location: mib\mib_ipnetrow.htm
tech.root: MIB
ms.assetid: aa9aa9f9-2334-4b08-896f-f4a77caa0f7f
ms.date: 08/03/2022
ms.keywords: '*PMIB_IPNETROW, *PMIB_IPNETROW_W2K, MIB_IPNETROW, MIB_IPNETROW structure [MIB], MIB_IPNETROW_W2K, MIB_IPNET_TYPE_DYNAMIC, MIB_IPNET_TYPE_INVALID, MIB_IPNET_TYPE_OTHER, MIB_IPNET_TYPE_STATIC, PMIB_IPNETROW, PMIB_IPNETROW structure pointer [MIB], _mpr_mib_ipnetrow, ipmib/MIB_IPNETROW, ipmib/PMIB_IPNETROW, iprtrmib/MIB_IPNETROW, iprtrmib/PMIB_IPNETROW, mib.mib_ipnetrow, rras.mib_ipnetrow'
req.header: ipmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MIB_IPNETROW_W2K, *PMIB_IPNETROW_W2K
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPNETROW_W2K
 - ipmib/_MIB_IPNETROW_W2K
 - PMIB_IPNETROW_W2K
 - ipmib/PMIB_IPNETROW_W2K
 - MIB_IPNETROW_W2K
 - ipmib/MIB_IPNETROW_W2K
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipmib.h
 - Iprtrmib.h
api_name:
 - MIB_IPNETROW
---

# MIB_IPNETROW_W2K structure


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

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipnetentry">CreateIpNetEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipnetentry">DeleteIpNetEntry</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipnettable">MIB_IPNETTABLE</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipnetentry">SetIpNetEntry</a>
