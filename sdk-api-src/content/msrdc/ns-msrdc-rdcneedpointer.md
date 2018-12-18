---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0006
title: RdcNeedPointer
author: windows-sdk-content
description: Describes an array of RdcNeed structures.
old-location: rdc\rdcneedpointer.htm
tech.root: rdc
ms.assetid: 92a1fae7-5ada-4f7d-a736-c93bc404a418
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RdcNeedPointer, RdcNeedPointer structure [Remote Differential Compression], fs.rdcneedpointer, msrdc/RdcNeedPointer, rdc.rdcneedpointer
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
 - RdcNeedPointer
product: Windows
targetos: Windows
req.typenames: RdcNeedPointer
req.redist: 
---

# RdcNeedPointer structure


## -description


The <b>RdcNeedPointer</b> structure describes an array 
    of <a href="https://msdn.microsoft.com/086e82f1-b033-48e2-b648-895c04751cc9">RdcNeed</a> structures. The 
    <b>RdcNeedPointer</b> structure is used as both input and output 
    by the <a href="https://msdn.microsoft.com/cc98a90c-ba82-4b92-a56c-07496a843089">IRdcComparator::Process</a> method.


## -struct-fields




### -field m_Size

Contains the number of <a href="https://msdn.microsoft.com/086e82f1-b033-48e2-b648-895c04751cc9">RdcNeed</a> structures in array pointed 
      to by <b>m_Data</b>.


### -field m_Used

When the structure is passed to the 
      <a href="https://msdn.microsoft.com/cc98a90c-ba82-4b92-a56c-07496a843089">IRdcComparator::Process</a> method, this member 
      should be zero. On return this member will contain the number of 
      <a href="https://msdn.microsoft.com/086e82f1-b033-48e2-b648-895c04751cc9">RdcNeed</a> structures that were filled with data.


### -field m_Data

Address of array of <a href="https://msdn.microsoft.com/086e82f1-b033-48e2-b648-895c04751cc9">RdcNeed</a> structures that describe the 
      chunks required from the source and seed data.


## -see-also




<a href="https://msdn.microsoft.com/cc98a90c-ba82-4b92-a56c-07496a843089">IRdcComparator::Process</a>



<a href="https://msdn.microsoft.com/086e82f1-b033-48e2-b648-895c04751cc9">RdcNeed</a>



<a href="https://msdn.microsoft.com/5144a94b-4af8-4ac2-b5b3-f0674a51c03b">Remote Differential Compression Structures</a>
 

 

