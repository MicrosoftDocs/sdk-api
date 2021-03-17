---
UID: NS:nldef._NL_INTERFACE_OFFLOAD_ROD
title: NL_INTERFACE_OFFLOAD_ROD (nldef.h)
description: Specifies a set of flags that indicate the offload capabilities for an IP interface.
helpviewer_keywords: ["*PNL_INTERFACE_OFFLOAD_ROD","NL_INTERFACE_OFFLOAD_ROD","NL_INTERFACE_OFFLOAD_ROD structure [MIB]","PNL_INTERFACE_OFFLOAD_ROD","PNL_INTERFACE_OFFLOAD_ROD structure pointer [MIB]","mib.nl_interface_offload_rod","nldef/NL_INTERFACE_OFFLOAD_ROD","nldef/PNL_INTERFACE_OFFLOAD_ROD"]
old-location: mib\nl_interface_offload_rod.htm
tech.root: MIB
ms.assetid: 764c7f5a-00df-461d-99ee-07f9e1f77ec7
ms.date: 12/05/2018
ms.keywords: '*PNL_INTERFACE_OFFLOAD_ROD, NL_INTERFACE_OFFLOAD_ROD, NL_INTERFACE_OFFLOAD_ROD structure [MIB], PNL_INTERFACE_OFFLOAD_ROD, PNL_INTERFACE_OFFLOAD_ROD structure pointer [MIB], mib.nl_interface_offload_rod, nldef/NL_INTERFACE_OFFLOAD_ROD, nldef/PNL_INTERFACE_OFFLOAD_ROD'
req.header: nldef.h
req.include-header: Iphlpapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NL_INTERFACE_OFFLOAD_ROD, *PNL_INTERFACE_OFFLOAD_ROD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NL_INTERFACE_OFFLOAD_ROD
 - nldef/_NL_INTERFACE_OFFLOAD_ROD
 - PNL_INTERFACE_OFFLOAD_ROD
 - nldef/PNL_INTERFACE_OFFLOAD_ROD
 - NL_INTERFACE_OFFLOAD_ROD
 - nldef/NL_INTERFACE_OFFLOAD_ROD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nldef.h
api_name:
 - NL_INTERFACE_OFFLOAD_ROD
---

# NL_INTERFACE_OFFLOAD_ROD structure


## -description

The <b>NL_INTERFACE_OFFLOAD_ROD</b> structure  specifies a set of flags that indicate the offload capabilities for an IP interface.

## -struct-fields

### -field NlChecksumSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports the offload of IP checksum calculations.

### -field NlOptionsSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports the offload of IP checksum calculations for IPv4 packets with IP options.

### -field TlDatagramChecksumSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports the offload of UDP checksum calculations.

### -field TlStreamChecksumSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports the offload of TCP checksum calculations.

### -field TlStreamOptionsSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports the offload of TCP checksum calculations for IPv4 packets containing IP options.

### -field FastPathCompatible

Type: <b>BOOLEAN</b>

Reserved for internal use.

### -field TlLargeSendOffloadSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports TCP Large Send Offload Version 1. With this capability, TCP can pass a buffer to be transmitted that is bigger than the maximum transmission unit (MTU) supported by the medium.  Version 1 allows TCP to pass a buffer up to 64K to be transmitted.

### -field TlGiantSendOffloadSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports TCP Large Send Offload Version 2. With this capability, TCP can pass a buffer to be transmitted that is bigger than the maximum transmission unit (MTU) supported by the medium.  Version 2 allows TCP to pass a buffer up to 256K to be transmitted. 





## -remarks

The <b>NL_INTERFACE_OFFLOAD_ROD</b> structure is defined on Windows Vista and later.

## -see-also

<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a>