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

# D3D12_PIPELINE_STATE_STREAM_DESC structure


## -description


Describes a pipeline state stream.


## -struct-fields




### -field SizeInBytes

<a href="https://msdn.microsoft.com/en-us/library/jj159528.aspx">SAL</a>: <code>_In_</code>

Specifies the size of the opaque data structure pointed to by the pPipelineStateSubobjectStream member, in bytes.


### -field pPipelineStateSubobjectStream

<a href="https://msdn.microsoft.com/en-us/library/jj159528.aspx">SAL</a>: <code>_In_reads_(_Inexpressible_("Dependentonsizeofsubobjects"))</code>

Specifies the address of a data structure that describes as a bytestream an arbitrary pipeline state subobject.


## -remarks



Use this structure with the ID3D12Device1::CreatePipelineState method to create pipeline state objects.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

