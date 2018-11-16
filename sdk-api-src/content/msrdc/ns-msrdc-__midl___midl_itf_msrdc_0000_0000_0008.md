---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0008
title: "__MIDL___MIDL_itf_msrdc_0000_0000_0008"
author: windows-sdk-content
description: Describes an array of RdcSignature structures.
old-location: rdc\rdcsignaturepointer.htm
tech.root: Rdc
ms.assetid: ece0fddf-1c06-493d-aed9-6bc86bb014f3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: RdcSignaturePointer, RdcSignaturePointer structure [Remote Differential Compression], __MIDL___MIDL_itf_msrdc_0000_0000_0008, fs.rdcsignaturepointer, msrdc/RdcSignaturePointer, rdc.rdcsignaturepointer
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
 - RdcSignaturePointer
product: Windows
targetos: Windows
req.typenames: RdcSignaturePointer
req.redist: 
---

# __MIDL___MIDL_itf_msrdc_0000_0000_0008 structure


## -description


The 
   <b>RdcSignaturePointer</b> structure
   describes an array 
    of <a href="https://msdn.microsoft.com/eca15d66-1d8c-422b-a2ab-7dbe00cb4087">RdcSignature</a> structures. The 
    <b>RdcSignaturePointer</b> structure is used as both input 
    and output by the 
    <a href="https://msdn.microsoft.com/566a5442-b186-4aac-94fa-5784736a30c3">IRdcSignatureReader::ReadSignatures</a> 
    method.


## -struct-fields




### -field m_Size

Contains the number of <a href="https://msdn.microsoft.com/eca15d66-1d8c-422b-a2ab-7dbe00cb4087">RdcSignature</a> structures in 
      array pointed to by <b>m_Data</b>.


### -field m_Used

When the structure is passed to the 
      <a href="https://msdn.microsoft.com/566a5442-b186-4aac-94fa-5784736a30c3">IRdcSignatureReader::ReadSignatures</a> 
      method, this member should be zero. On return this member will contain the number of 
      <a href="https://msdn.microsoft.com/eca15d66-1d8c-422b-a2ab-7dbe00cb4087">RdcSignature</a> structures that were filled.


### -field m_Data

Address of an array of <a href="https://msdn.microsoft.com/eca15d66-1d8c-422b-a2ab-7dbe00cb4087">RdcSignature</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/566a5442-b186-4aac-94fa-5784736a30c3">IRdcSignatureReader::ReadSignatures</a>



<a href="https://msdn.microsoft.com/eca15d66-1d8c-422b-a2ab-7dbe00cb4087">RdcSignature</a>



<a href="https://msdn.microsoft.com/5144a94b-4af8-4ac2-b5b3-f0674a51c03b">Remote Differential Compression Structures</a>
 

 

