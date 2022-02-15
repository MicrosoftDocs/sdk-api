---
UID: NS:ipmib._MIB_IPMCAST_MFE
title: MIB_IPMCAST_MFE (ipmib.h)
description: Stores the information for an Internet Protocol (IP) Multicast Forwarding Entry (MFE).
helpviewer_keywords: ["*PMIB_IPMCAST_MFE","MIB_IPMCAST_MFE","MIB_IPMCAST_MFE structure [MIB]","PMIB_IPMCAST_MFE","PMIB_IPMCAST_MFE structure pointer [MIB]","_mpr_mib_ipmcast_mfe","ipmib/MIB_IPMCAST_MFE","ipmib/PMIB_IPMCAST_MFE","iprtrmib/MIB_IPMCAST_MFE","iprtrmib/PMIB_IPMCAST_MFE","mib.mib_ipmcast_mfe","rras.mib_ipmcast_mfe"]
old-location: mib\mib_ipmcast_mfe.htm
tech.root: MIB
ms.assetid: 731e2c88-5c4f-4165-a9f2-287b4c10c76b
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPMCAST_MFE, MIB_IPMCAST_MFE, MIB_IPMCAST_MFE structure [MIB], PMIB_IPMCAST_MFE, PMIB_IPMCAST_MFE structure pointer [MIB], _mpr_mib_ipmcast_mfe, ipmib/MIB_IPMCAST_MFE, ipmib/PMIB_IPMCAST_MFE, iprtrmib/MIB_IPMCAST_MFE, iprtrmib/PMIB_IPMCAST_MFE, mib.mib_ipmcast_mfe, rras.mib_ipmcast_mfe'
req.header: ipmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: MIB_IPMCAST_MFE, *PMIB_IPMCAST_MFE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPMCAST_MFE
 - ipmib/_MIB_IPMCAST_MFE
 - PMIB_IPMCAST_MFE
 - ipmib/PMIB_IPMCAST_MFE
 - MIB_IPMCAST_MFE
 - ipmib/MIB_IPMCAST_MFE
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
 - MIB_IPMCAST_MFE
---

# MIB_IPMCAST_MFE structure


## -description

The 
<b>MIB_IPMCAST_MFE</b> structure stores the information for an Internet Protocol (IP) Multicast Forwarding Entry (MFE).

## -struct-fields

### -field dwGroup

Type: <b>DWORD</b>

The range of IPv4 multicast groups for this MFE. A value of zero indicates a wildcard group.

### -field dwSource

Type: <b>DWORD</b>

The range of IPv4 source addresses for this MFE. A value of zero indicates a wildcard source.

### -field dwSrcMask

Type: <b>DWORD</b>

The IPv4 subnet mask that corresponds to <b>dwSourceAddr</b>. The <b>dwSourceAddr</b> and <b>dwSourceMask</b> members are used together to define a range of sources.

### -field dwUpStrmNgbr

Type: <b>DWORD</b>

The upstream neighbor that is related to this MFE.

### -field dwInIfIndex

Type: <b>DWORD</b>

The index of the interface to which this MFE is related.

### -field dwInIfProtocol

Type: <b>DWORD</b>

The routing protocol that owns the incoming interface to which this MFE is related.

### -field dwRouteProtocol

Type: <b>DWORD</b>

The client that created the route.

### -field dwRouteNetwork

Type: <b>DWORD</b>

The IPv4 address associated with the route referred to by <b>dwRouteProtocol</b>.

### -field dwRouteMask

Type: <b>DWORD</b>

The IPv4 mask associated with the route referred to by <b>dwRouteProtocol</b>.

### -field ulUpTime

Type: <b>ULONG</b>

The time, in seconds, this MFE has been valid. This value starts from zero and is incremented until it reaches the <b>ulTimeOut</b> value, at which time the MFE is deleted.

### -field ulExpiryTime

Type: <b>ULONG</b>

The time, in seconds, that remains before the MFE expires and is deleted. This value starts from <b>ulTimeOut</b> and is decremented until it reaches zero, at which time the MFE is deleted.

### -field ulTimeOut

Type: <b>ULONG</b>

The total length of time, in seconds, that this MFE should remain valid. After the time-out value is exceeded, the MFE is deleted. This value is static.

### -field ulNumOutIf

Type: <b>ULONG</b>

The number of outgoing interfaces that are associated with this MFE.

### -field fFlags

Type: <b>DWORD</b>

Reserved. This member should be <b>NULL</b>.

### -field dwReserved

Type: <b>DWORD</b>

Reserved. This member should be <b>NULL</b>.

### -field rgmioOutInfo

Type: <b>MIB_IPMCAST_OIF[ANY_SIZE]</b>

A pointer to a table of outgoing interface statistics that are implemented as an array of 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_oif_w2k">MIB_IPMCAST_OIF</a> structures.

## -remarks

The 
<b>MIB_IPMCAST_MFE</b> structure does not have a fixed size. Use the <b>SIZEOF_MIB_MFE(X)</b> macro to determine the size of this structure. This macro is defined in the Iprtrmib.h header file.

The <b>dwRouteProtocol</b>, <b>dwRouteNetwork</b>, and <b>dwRouteMask</b> members uniquely identify the route to which this MFE is related.

The <b>MIB_IPMCAST_MFE</b> structure is used by the <a href="/windows/desktop/RRAS/multicast-group-manager-functions">Multicast Group Manager functions</a>. The <b>MIB_IPMCAST_MFE</b> structure is retrieved using the <a href="/windows/desktop/api/mgm/nf-mgm-mgmgetmfe">MgmGetMfe</a> function. An existing <b>MIB_IPMCAST_MFE</b> structure can be modified using the <a href="/windows/desktop/api/mgm/nf-mgm-mgmsetmfe">MgmSetMfe</a> function.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_oif_w2k">MIB_IPMCAST_OIF</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_mfe_table">MIB_MFE_TABLE</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgetmfe">MgmGetMfe</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmsetmfe">MgmSetMfe</a>



<a href="/windows/desktop/RRAS/multicast-group-manager-functions">Multicast Group Manager functions</a>