---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0004
title: RdcNeed (msrdc.h)
description: Contains information about a chunk that is required to synchronize two sets of data.
old-location: rdc\rdcneed.htm
tech.root: rdc
ms.assetid: 086e82f1-b033-48e2-b648-895c04751cc9
ms.date: 12/05/2018
ms.keywords: RdcNeed, RdcNeed structure [Remote Differential Compression], fs.rdcneed, msrdc/RdcNeed, rdc.rdcneed
f1_keywords:
- msrdc/RdcNeed
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- MsRdc.h
api_name:
- RdcNeed
targetos: Windows
req.typenames: RdcNeed
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/win32/api/msrdc/ns-msrdc-rdcneedpointer">RdcNeedPointer</a>



<a href="https://docs.microsoft.com/windows/win32/api/msrdc/ne-msrdc-rdcneedtype">RdcNeedType</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/rdc/remote-differential-compression-structures">Remote Differential Compression Structures</a>
 

 

