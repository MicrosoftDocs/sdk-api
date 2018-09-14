---
UID: NF:d3d10effect.ID3D10EffectVariable.GetAnnotationByName
title: ID3D10EffectVariable::GetAnnotationByName
author: windows-sdk-content
description: Get an annotation by name.
old-location: direct3d10\id3d10effectvariable_getannotationbyname.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getannotationbyname.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 88e41418-934c-2f28-baec-b4fa95311890, GetAnnotationByName, GetAnnotationByName method [Direct3D 10], GetAnnotationByName method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetAnnotationByName method, ID3D10EffectVariable.GetAnnotationByName, ID3D10EffectVariable::GetAnnotationByName, d3d10effect/ID3D10EffectVariable::GetAnnotationByName, direct3d10.id3d10effectvariable_getannotationbyname
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectVariable.GetAnnotationByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectVariable::GetAnnotationByName


## -description


Get an annotation by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The annotation name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>.  Note that if the annotation is not found the <b>ID3D10EffectVariable Interface</b> returned will be empty. The <a href="https://msdn.microsoft.com/en-us/library/Bb173746(v=VS.85).aspx">ID3D10EffectVariable::IsValid</a> method should be called to determine whether the annotation was found.




## -remarks



Annonations can be attached to a technique, a pass or a gloval variable. For the syntax, see <a href="https://msdn.microsoft.com/en-us/library/Bb205046(v=VS.85).aspx">Annotation Syntax (Direct3D 10)</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>
 

 

