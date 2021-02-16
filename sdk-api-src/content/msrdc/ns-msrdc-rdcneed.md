---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0004
title: RdcNeed (msrdc.h)
description: Contains information about a chunk that is required to synchronize two sets of data.
helpviewer_keywords: ["RdcNeed","RdcNeed structure [Remote Differential Compression]","fs.rdcneed","msrdc/RdcNeed","rdc.rdcneed"]
old-location: rdc\rdcneed.htm
tech.root: rdc
ms.assetid: 086e82f1-b033-48e2-b648-895c04751cc9
ms.date: 12/05/2018
ms.keywords: RdcNeed, RdcNeed structure [Remote Differential Compression], fs.rdcneed, msrdc/RdcNeed, rdc.rdcneed
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
req.typenames: RdcNeed
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msrdc_0000_0000_0004
 - msrdc/__MIDL___MIDL_itf_msrdc_0000_0000_0004
 - RdcNeed
 - msrdc/RdcNeed
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
 - RdcNeed
---

# RdcNeed structure


## -description

The <b>RdcNeed</b> structure contains information about a 
    chunk that is required to synchronize two sets of data.

## -struct-fields

### -field m_BlockType

Describes the type of data needed—source data or seed data.

### -field m_FileOffset

Offset, in bytes, from the start of the data where the chunk should be copied from.

### -field m_BlockLength

Length, in bytes, of the chunk of data that is to be copied to the target data.

## -see-also

<a href="/windows/win32/api/msrdc/ns-msrdc-rdcneedpointer">RdcNeedPointer</a>



<a href="/windows/win32/api/msrdc/ne-msrdc-rdcneedtype">RdcNeedType</a>



<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-structures">Remote Differential Compression Structures</a>