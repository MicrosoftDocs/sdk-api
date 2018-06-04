---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

