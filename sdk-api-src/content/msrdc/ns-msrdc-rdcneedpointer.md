---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0006
title: RdcNeedPointer (msrdc.h)
description: Describes an array of RdcNeed structures.
helpviewer_keywords: ["RdcNeedPointer","RdcNeedPointer structure [Remote Differential Compression]","fs.rdcneedpointer","msrdc/RdcNeedPointer","rdc.rdcneedpointer"]
old-location: rdc\rdcneedpointer.htm
tech.root: rdc
ms.assetid: 92a1fae7-5ada-4f7d-a736-c93bc404a418
ms.date: 12/05/2018
ms.keywords: RdcNeedPointer, RdcNeedPointer structure [Remote Differential Compression], fs.rdcneedpointer, msrdc/RdcNeedPointer, rdc.rdcneedpointer
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
req.typenames: RdcNeedPointer
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msrdc_0000_0000_0006
 - msrdc/__MIDL___MIDL_itf_msrdc_0000_0000_0006
 - RdcNeedPointer
 - msrdc/RdcNeedPointer
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
 - RdcNeedPointer
---

# RdcNeedPointer structure


## -description

The <b>RdcNeedPointer</b> structure describes an array 
    of <a href="/windows/win32/api/msrdc/ns-msrdc-rdcneed">RdcNeed</a> structures. The 
    <b>RdcNeedPointer</b> structure is used as both input and output 
    by the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdccomparator-process">IRdcComparator::Process</a> method.

## -struct-fields

### -field m_Size

Contains the number of <a href="/windows/win32/api/msrdc/ns-msrdc-rdcneed">RdcNeed</a> structures in array pointed 
      to by <b>m_Data</b>.

### -field m_Used

When the structure is passed to the 
      <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdccomparator-process">IRdcComparator::Process</a> method, this member 
      should be zero. On return this member will contain the number of 
      <a href="/windows/win32/api/msrdc/ns-msrdc-rdcneed">RdcNeed</a> structures that were filled with data.

### -field m_Data

Address of array of <a href="/windows/win32/api/msrdc/ns-msrdc-rdcneed">RdcNeed</a> structures that describe the 
      chunks required from the source and seed data.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdccomparator-process">IRdcComparator::Process</a>



<a href="/windows/win32/api/msrdc/ns-msrdc-rdcneed">RdcNeed</a>



<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-structures">Remote Differential Compression Structures</a>