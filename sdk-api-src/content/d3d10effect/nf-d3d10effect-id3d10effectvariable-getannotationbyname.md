---
UID: NF:d3d10effect.ID3D10EffectVariable.GetAnnotationByName
title: ID3D10EffectVariable::GetAnnotationByName
author: windows-sdk-content
description: Get an annotation by name.
old-location: direct3d10\id3d10effectvariable_getannotationbyname.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getannotationbyname.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 88e41418-934c-2f28-baec-b4fa95311890, GetAnnotationByName, GetAnnotationByName method [Direct3D 10], GetAnnotationByName method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetAnnotationByName method, ID3D10EffectVariable.GetAnnotationByName, ID3D10EffectVariable::GetAnnotationByName, d3d10effect/ID3D10EffectVariable::GetAnnotationByName, direct3d10.id3d10effectvariable_getannotationbyname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
req.include-header: 
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10Effect.h
api_name:
-	ID3D10EffectVariable.GetAnnotationByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVariable::GetAnnotationByName


## -description


Get an annotation by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The annotation name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>.  Note that if the annotation is not found the <b>ID3D10EffectVariable Interface</b> returned will be empty. The <a href="https://msdn.microsoft.com/b27f1669-94a1-4971-bd8f-e5a56f43560f">ID3D10EffectVariable::IsValid</a> method should be called to determine whether the annotation was found.




## -remarks



Annonations can be attached to a technique, a pass or a gloval variable. For the syntax, see <a href="https://msdn.microsoft.com/9178e61e-05a4-441c-a9f1-e05e23ab48a5">Annotation Syntax (Direct3D 10)</a>.




## -see-also




<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>
 

 

