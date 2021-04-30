---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0008
title: RdcSignaturePointer (msrdc.h)
description: Describes an array of RdcSignature structures.
helpviewer_keywords: ["RdcSignaturePointer","RdcSignaturePointer structure [Remote Differential Compression]","fs.rdcsignaturepointer","msrdc/RdcSignaturePointer","rdc.rdcsignaturepointer"]
old-location: rdc\rdcsignaturepointer.htm
tech.root: rdc
ms.assetid: ece0fddf-1c06-493d-aed9-6bc86bb014f3
ms.date: 12/05/2018
ms.keywords: RdcSignaturePointer, RdcSignaturePointer structure [Remote Differential Compression], fs.rdcsignaturepointer, msrdc/RdcSignaturePointer, rdc.rdcsignaturepointer
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
req.typenames: RdcSignaturePointer
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msrdc_0000_0000_0008
 - msrdc/__MIDL___MIDL_itf_msrdc_0000_0000_0008
 - RdcSignaturePointer
 - msrdc/RdcSignaturePointer
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
 - RdcSignaturePointer
---

# RdcSignaturePointer structure


## -description

The 
   <b>RdcSignaturePointer</b> structure
   describes an array 
    of <a href="/windows/win32/api/msrdc/ns-msrdc-rdcsignature">RdcSignature</a> structures. The 
    <b>RdcSignaturePointer</b> structure is used as both input 
    and output by the 
    <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcsignaturereader-readsignatures">IRdcSignatureReader::ReadSignatures</a> 
    method.

## -struct-fields

### -field m_Size

Contains the number of <a href="/windows/win32/api/msrdc/ns-msrdc-rdcsignature">RdcSignature</a> structures in 
      array pointed to by <b>m_Data</b>.

### -field m_Used

When the structure is passed to the 
      <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcsignaturereader-readsignatures">IRdcSignatureReader::ReadSignatures</a> 
      method, this member should be zero. On return this member will contain the number of 
      <a href="/windows/win32/api/msrdc/ns-msrdc-rdcsignature">RdcSignature</a> structures that were filled.

### -field m_Data

Address of an array of <a href="/windows/win32/api/msrdc/ns-msrdc-rdcsignature">RdcSignature</a> structures.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcsignaturereader-readsignatures">IRdcSignatureReader::ReadSignatures</a>



<a href="/windows/win32/api/msrdc/ns-msrdc-rdcsignature">RdcSignature</a>



<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-structures">Remote Differential Compression Structures</a>