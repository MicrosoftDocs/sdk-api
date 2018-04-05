---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0005
title: "__MIDL___MIDL_itf_msrdc_0000_0000_0005"
author: windows-driver-content
description: Describes a buffer.
old-location: rdc\rdcbufferpointer.htm
old-project: Rdc
ms.assetid: 1792e40b-c363-4732-9613-301c3e6e4da7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: RdcBufferPointer, RdcBufferPointer structure [Remote Differential Compression], __MIDL___MIDL_itf_msrdc_0000_0000_0005, fs.rdcbufferpointer, msrdc/RdcBufferPointer, rdc.rdcbufferpointer
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
req.typenames: RdcBufferPointer
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	MsRdc.h
api_name:
-	RdcBufferPointer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# __MIDL___MIDL_itf_msrdc_0000_0000_0005 structure


## -description


The <b>RdcBufferPointer</b> structure describes a 
    buffer.


## -struct-fields




### -field m_Size

Size, in bytes, of the buffer.


### -field m_Used

For input buffers, <a href="https://msdn.microsoft.com/cc98a90c-ba82-4b92-a56c-07496a843089">IRdcComparator::Process</a> 
      and <a href="https://msdn.microsoft.com/34d19eee-0fa9-4ac3-a33b-9f01cfa06371">IRdcGenerator::Process</a> will store here how 
      much (if any) of the buffer was used during processing.


### -field m_Data

Pointer to the buffer.


## -see-also




<a href="https://msdn.microsoft.com/5144a94b-4af8-4ac2-b5b3-f0674a51c03b">Remote Differential Compression Structures</a>
 

 

