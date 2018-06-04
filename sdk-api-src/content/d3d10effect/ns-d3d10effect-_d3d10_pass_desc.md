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

# _D3D10_PASS_DESC structure


## -description


Describes an effect pass, which contains pipeline state.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A string that contains the name of the pass; otherwise <b>NULL</b>.


### -field Annotations

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of annotations.


### -field pIAInputSignature

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a>*</b>

A pointer to the input signature or the vertex shader; otherwise <b>NULL</b>.


### -field IAInputSignatureSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The size of the input signature (in bytes).


### -field StencilRef

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The stencil-reference value used in the depth-stencil state (see <a href="https://msdn.microsoft.com/e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f">Configuring Depth-Stencil Functionality (Direct3D 10)</a>).


### -field SampleMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The sample mask for the blend state (see <a href="https://msdn.microsoft.com/f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3">Configuring Blending Functionality (Direct3D 10)</a>).


### -field BlendFactor

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

The per-component blend factors (RGBA) for the blend state (see <a href="https://msdn.microsoft.com/f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3">Configuring Blending Functionality (Direct3D 10)</a>).


## -remarks



Get a pass description by calling <a href="https://msdn.microsoft.com/40744216-0199-4667-a4ad-69a56811b52c">ID3D10EffectPass::GetDesc</a>; an effect technique contains one or more passes.




## -see-also




<a href="https://msdn.microsoft.com/bbd69b4b-d2f4-471f-a607-328f5fc603b5">Effect Structures (Direct3D 10)</a>
 

 

