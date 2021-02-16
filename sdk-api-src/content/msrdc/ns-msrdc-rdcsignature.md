---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0007
title: RdcSignature (msrdc.h)
description: Contains a single signature and the length of the chunk used to generate it.
helpviewer_keywords: ["RdcSignature","RdcSignature structure [Remote Differential Compression]","fs.rdcsignature","msrdc/RdcSignature","rdc.rdcsignature"]
old-location: rdc\rdcsignature.htm
tech.root: rdc
ms.assetid: eca15d66-1d8c-422b-a2ab-7dbe00cb4087
ms.date: 12/05/2018
ms.keywords: RdcSignature, RdcSignature structure [Remote Differential Compression], fs.rdcsignature, msrdc/RdcSignature, rdc.rdcsignature
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
req.typenames: RdcSignature
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msrdc_0000_0000_0007
 - msrdc/__MIDL___MIDL_itf_msrdc_0000_0000_0007
 - RdcSignature
 - msrdc/RdcSignature
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
 - RdcSignature
---

# RdcSignature structure


## -description

The <b>RdcSignature</b> structure contains a single 
    signature and the length of the chunk used to generate it.

## -struct-fields

### -field m_Signature

Signature of a chunk of data.

### -field m_BlockLength

Length of the chunk represented by this signature.

## -see-also

<a href="/windows/win32/api/msrdc/ns-msrdc-rdcsignaturepointer">RdcSignaturePointer</a>



<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-structures">Remote Differential Compression Structures</a>