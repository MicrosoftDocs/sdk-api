---
UID: NE:clusapi.CLUSPROP_IPADDR_ENABLENETBIOS
title: CLUSPROP_IPADDR_ENABLENETBIOS (clusapi.h)
description: When used with the CLUSPROP_DWORD structure, enables or disables the functionality of the EnableNetBIOS property of IP Address resources.
helpviewer_keywords: ["CLUSPROP_IPADDR_ENABLENETBIOS","CLUSPROP_IPADDR_ENABLENETBIOS enumeration [Failover Cluster]","CLUSPROP_IPADDR_ENABLENETBIOS_DISABLED","CLUSPROP_IPADDR_ENABLENETBIOS_ENABLED","CLUSPROP_IPADDR_ENABLENETBIOS_TRACK_NIC","clusapi/CLUSPROP_IPADDR_ENABLENETBIOS","clusapi/CLUSPROP_IPADDR_ENABLENETBIOS_DISABLED","clusapi/CLUSPROP_IPADDR_ENABLENETBIOS_ENABLED","clusapi/CLUSPROP_IPADDR_ENABLENETBIOS_TRACK_NIC","mscs.clusprop_ipaddr_enablenetbios"]
old-location: mscs\clusprop_ipaddr_enablenetbios.htm
tech.root: MsCS
ms.assetid: 4d1610f0-6a7c-4dfa-9fec-4165f28dd7de
ms.date: 12/05/2018
ms.keywords: CLUSPROP_IPADDR_ENABLENETBIOS, CLUSPROP_IPADDR_ENABLENETBIOS enumeration [Failover Cluster], CLUSPROP_IPADDR_ENABLENETBIOS_DISABLED, CLUSPROP_IPADDR_ENABLENETBIOS_ENABLED, CLUSPROP_IPADDR_ENABLENETBIOS_TRACK_NIC, clusapi/CLUSPROP_IPADDR_ENABLENETBIOS, clusapi/CLUSPROP_IPADDR_ENABLENETBIOS_DISABLED, clusapi/CLUSPROP_IPADDR_ENABLENETBIOS_ENABLED, clusapi/CLUSPROP_IPADDR_ENABLENETBIOS_TRACK_NIC, mscs.clusprop_ipaddr_enablenetbios
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
req.typenames: CLUSPROP_IPADDR_ENABLENETBIOS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_IPADDR_ENABLENETBIOS
 - clusapi/CLUSPROP_IPADDR_ENABLENETBIOS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSPROP_IPADDR_ENABLENETBIOS
---

# CLUSPROP_IPADDR_ENABLENETBIOS enumeration


## -description

When used with the <a href="/previous-versions/windows/desktop/legacy/aa368375(v=vs.85)">CLUSPROP_DWORD</a> structure, 
    enables or disables the functionality of the 
    <a href="/previous-versions/windows/desktop/mscs/ip-addresses-enablenetbios">EnableNetBIOS</a> property of 
    <a href="/previous-versions/windows/desktop/mscs/ip-address">IP Address</a> <a href="/previous-versions/windows/desktop/mscs/resources">resources</a>.

## -enum-fields

### -field CLUSPROP_IPADDR_ENABLENETBIOS_DISABLED:0

Disable the functionality of the 
       <a href="/previous-versions/windows/desktop/mscs/ip-addresses-enablenetbios">EnableNetBIOS</a> property.

### -field CLUSPROP_IPADDR_ENABLENETBIOS_ENABLED

Enable the functionality of the 
       <a href="/previous-versions/windows/desktop/mscs/ip-addresses-enablenetbios">EnableNetBIOS</a> property.

### -field CLUSPROP_IPADDR_ENABLENETBIOS_TRACK_NIC

Enable the functionality of the 
       <a href="/previous-versions/windows/desktop/mscs/ip-addresses-enablenetbios">EnableNetBIOS</a> property if the NIC to 
       which the IP Address resource is bound has enabled NetBIOS.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/ip-addresses-enablenetbios">EnableNetBIOS</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
