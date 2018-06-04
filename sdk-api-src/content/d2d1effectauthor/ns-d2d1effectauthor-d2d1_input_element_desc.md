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

# D2D1_INPUT_ELEMENT_DESC structure


## -description


A description of a single element to the vertex layout.


## -struct-fields




### -field semanticName

The <a href="https://msdn.microsoft.com/6f5c504c-1940-4d1c-b594-a2132599376b">HLSL semantic</a> associated with this element in a <a href="https://msdn.microsoft.com/c73a4f3e-e6fa-4e49-9ee8-4e200269dba7">shader input-signature</a>.


### -field semanticIndex

The semantic index for the element. A semantic index modifies a semantic, with an integer index number. A semantic index is only needed in a case where there is more than one element with the same semantic. For example, a 4x4 matrix would have four components each with the semantic name matrix; however, each of the four components would have different semantic indices (0, 1, 2, and 3).


### -field format

The data type of the element data.


### -field inputSlot

An integer value that identifies the input-assembler. Valid values are between 0 and 15.


### -field alignedByteOffset

The offset in bytes between each element.


## -remarks



This structure is a subset of <a href="https://msdn.microsoft.com/45545d24-1513-4efd-9344-20673c5b98d5">D3D11_INPUT_ELEMENT_DESC</a> that omits fields required to define a vertex layout.

If the <a href="direct2d_constants.htm">D2D1_APPEND_ALIGNED_ELEMENT</a> constant is used for  <b>alignedByteOffset</b>, the elements will be packed contiguously for convenience.





## -see-also




<a href="https://msdn.microsoft.com/ff122e0d-5f0e-4a61-bead-53bea6f1648f">D2D1_VERTEX_USAGE</a>



<a href="https://msdn.microsoft.com/84c0ca29-2356-4b7f-98ee-ff1758edc540">Getting Started with the Input-Assembler Stage</a>



<a href="https://msdn.microsoft.com/8E59527F-B6CE-4E25-B7F7-2D03BC1ACAFD">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="https://msdn.microsoft.com/60D3DB1B-D347-44FC-98F9-545D4213F1F0">ID2D1EffectContext::LoadVertexShader</a>



<a href="https://msdn.microsoft.com/6f5c504c-1940-4d1c-b594-a2132599376b">Semantics</a>



<a href="https://msdn.microsoft.com/c73a4f3e-e6fa-4e49-9ee8-4e200269dba7">Signatures</a>
 

 

