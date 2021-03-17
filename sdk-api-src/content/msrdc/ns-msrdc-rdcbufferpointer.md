---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0005
title: RdcBufferPointer (msrdc.h)
description: Describes a buffer.
helpviewer_keywords: ["RdcBufferPointer","RdcBufferPointer structure [Remote Differential Compression]","fs.rdcbufferpointer","msrdc/RdcBufferPointer","rdc.rdcbufferpointer"]
old-location: rdc\rdcbufferpointer.htm
tech.root: rdc
ms.assetid: 1792e40b-c363-4732-9613-301c3e6e4da7
ms.date: 12/05/2018
ms.keywords: RdcBufferPointer, RdcBufferPointer structure [Remote Differential Compression], fs.rdcbufferpointer, msrdc/RdcBufferPointer, rdc.rdcbufferpointer
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
req.typenames: RdcBufferPointer
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msrdc_0000_0000_0005
 - msrdc/__MIDL___MIDL_itf_msrdc_0000_0000_0005
 - RdcBufferPointer
 - msrdc/RdcBufferPointer
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
 - RdcBufferPointer
---

# RdcBufferPointer structure


## -description

The <b>RdcBufferPointer</b> structure describes a 
    buffer.

## -struct-fields

### -field m_Size

Size, in bytes, of the buffer.

### -field m_Used

For input buffers, <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdccomparator-process">IRdcComparator::Process</a> 
      and <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgenerator-process">IRdcGenerator::Process</a> will store here how 
      much (if any) of the buffer was used during processing.

### -field m_Data

Pointer to the buffer.

## -see-also

<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-structures">Remote Differential Compression Structures</a>