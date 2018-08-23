---
UID: NF:d3d10effect.ID3D10EffectVariable.GetMemberBySemantic
title: ID3D10EffectVariable::GetMemberBySemantic
author: windows-sdk-content
description: Get a structure member by semantic.
old-location: direct3d10\id3d10effectvariable_getmemberbysemantic.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getmemberbysemantic.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 39fcf4c4-6072-0377-d1b8-ca11cc848a0c, GetMemberBySemantic, GetMemberBySemantic method [Direct3D 10], GetMemberBySemantic method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetMemberBySemantic method, ID3D10EffectVariable.GetMemberBySemantic, ID3D10EffectVariable::GetMemberBySemantic, d3d10effect/ID3D10EffectVariable::GetMemberBySemantic, direct3d10.id3d10effectvariable_getmemberbysemantic
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
 - ID3D10EffectVariable.GetMemberBySemantic
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVariable::GetMemberBySemantic


## -description


Get a structure member by semantic.


## -parameters




### -param Semantic [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The semantic.


## -returns



Type: <b><a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>.




## -remarks



If the effect variable is an structure, use this method to look up a member by attached semantic.




## -see-also




<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>
 

 

