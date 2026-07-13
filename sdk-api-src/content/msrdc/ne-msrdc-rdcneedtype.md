---
UID: NE:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0003
title: RdcNeedType (msrdc.h)
description: Defines the set of data chunks used to generate a remote copy.
helpviewer_keywords: ["RDCNEED_SEED","RDCNEED_SEED_MAX","RDCNEED_SOURCE","RDCNEED_TARGET","RdcNeedType","RdcNeedType enumeration [Remote Differential Compression]","fs.rdcneedtype","msrdc/RDCNEED_SEED","msrdc/RDCNEED_SEED_MAX","msrdc/RDCNEED_SOURCE","msrdc/RDCNEED_TARGET","msrdc/RdcNeedType","rdc.rdcneedtype"]
old-location: rdc\rdcneedtype.htm
tech.root: rdc
ms.assetid: 93173b2e-a0df-445e-98a8-f7df02fbc7a8
ms.date: 12/05/2018
ms.keywords: RDCNEED_SEED, RDCNEED_SEED_MAX, RDCNEED_SOURCE, RDCNEED_TARGET, RdcNeedType, RdcNeedType enumeration [Remote Differential Compression], fs.rdcneedtype, msrdc/RDCNEED_SEED, msrdc/RDCNEED_SEED_MAX, msrdc/RDCNEED_SOURCE, msrdc/RDCNEED_TARGET, msrdc/RdcNeedType, rdc.rdcneedtype
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RdcNeedType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msrdc_0000_0000_0003
 - msrdc/__MIDL___MIDL_itf_msrdc_0000_0000_0003
 - RdcNeedType
 - msrdc/RdcNeedType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MsRdc.h
api_name:
 - RdcNeedType
---

# RdcNeedType enumeration


## -description

Defines the set of 
    data chunks used to generate a remote copy.

## -enum-fields

### -field RDCNEED_SOURCE:0

The chunk is a source chunk.

### -field RDCNEED_TARGET:1

This value is reserved for future use.

### -field RDCNEED_SEED:2

The chunk is a seed chunk.

### -field RDCNEED_SEED_MAX:255

This value is reserved for future use.

## -see-also

<a href="/windows/win32/api/msrdc/ns-msrdc-rdcneed">RdcNeed</a>



<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-enumerations">Remote Differential Compression Enumerations</a>
