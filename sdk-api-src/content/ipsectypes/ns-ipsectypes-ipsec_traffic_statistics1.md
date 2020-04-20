---
UID: NS:ipsectypes.IPSEC_TRAFFIC_STATISTICS1_
title: IPSEC_TRAFFIC_STATISTICS1 (ipsectypes.h)
description: Stores IPsec traffic statistics.helpviewer_keywords: ["IPSEC_TRAFFIC_STATISTICS1","IPSEC_TRAFFIC_STATISTICS1 structure [Filtering]","fwp.ipsec_traffic_statistics1_struct","ipsectypes/IPSEC_TRAFFIC_STATISTICS1"]
old-location: fwp\ipsec_traffic_statistics1_struct.htm
tech.root: fwp
ms.assetid: 3b25d98a-9216-4e74-91fc-cc8658e12d9b
ms.date: 12/05/2018
ms.keywords: IPSEC_TRAFFIC_STATISTICS1, IPSEC_TRAFFIC_STATISTICS1 structure [Filtering], fwp.ipsec_traffic_statistics1_struct, ipsectypes/IPSEC_TRAFFIC_STATISTICS1
f1_keywords:
- ipsectypes/IPSEC_TRAFFIC_STATISTICS1
dev_langs:
- c++
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Ipsectypes.h
api_name:
- IPSEC_TRAFFIC_STATISTICS1
targetos: Windows
req.typenames: IPSEC_TRAFFIC_STATISTICS1
req.redist: 
ms.custom: 19H1
---

# IPSEC_TRAFFIC_STATISTICS1 structure


## -description


The <b>IPSEC_TRAFFIC_STATISTICS1</b> structure stores IPsec traffic statistics.
[IPSEC_TRAFFIC_STATISTICS0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0)a> is available.</div><div> </div>

## -struct-fields




### -field encryptedByteCount

Specifies encrypted byte count.


### -field authenticatedAHByteCount

Specifies authenticated AH byte count.


### -field authenticatedESPByteCount

Specifies authenticated ESP byte count.


### -field transportByteCount

Specifies transport byte count.


### -field tunnelByteCount

Specifies tunnel byte count.


### -field offloadByteCount

Specifies offload byte count.


### -field totalSuccessfulPackets

The total number of packets that were successfully transmitted.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

