---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0007
title: "__MIDL___MIDL_itf_msrdc_0000_0000_0007"
author: windows-sdk-content
description: Contains a single signature and the length of the chunk used to generate it.
old-location: rdc\rdcsignature.htm
tech.root: rdc
ms.assetid: eca15d66-1d8c-422b-a2ab-7dbe00cb4087
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: RdcSignature, RdcSignature structure [Remote Differential Compression], __MIDL___MIDL_itf_msrdc_0000_0000_0007, fs.rdcsignature, msrdc/RdcSignature, rdc.rdcsignature
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - RdcSignature
product: Windows
targetos: Windows
req.typenames: RdcSignature
req.redist: 
---

# __MIDL___MIDL_itf_msrdc_0000_0000_0007 structure


## -description


The <b>RdcSignature</b> structure contains a single 
    signature and the length of the chunk used to generate it.


## -struct-fields




### -field m_Signature

Signature of a chunk of data.


### -field m_BlockLength

Length of the chunk represented by this signature.


## -see-also




<a href="https://msdn.microsoft.com/ece0fddf-1c06-493d-aed9-6bc86bb014f3">RdcSignaturePointer</a>



<a href="https://msdn.microsoft.com/5144a94b-4af8-4ac2-b5b3-f0674a51c03b">Remote Differential Compression Structures</a>
 

 

