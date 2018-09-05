---
UID: NF:d3d10effect.ID3D10EffectVariable.GetElement
title: ID3D10EffectVariable::GetElement
author: windows-sdk-content
description: Get an array element.
old-location: direct3d10\id3d10effectvariable_getelement.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getelement.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 9b0e159b-0d15-0249-35fe-c610c699f1ba, GetElement, GetElement method [Direct3D 10], GetElement method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetElement method, ID3D10EffectVariable.GetElement, ID3D10EffectVariable::GetElement, d3d10effect/ID3D10EffectVariable::GetElement, direct3d10.id3d10effectvariable_getelement
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectVariable.GetElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVariable::GetElement


## -description


Get an array element.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based index; otherwise 0.


## -returns



Type: <b><a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>.




## -remarks



If the effect variable is an array, use this method to return one of the elements.




## -see-also




<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>
 

 

