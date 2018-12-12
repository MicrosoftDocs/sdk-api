---
UID: NF:d3d10effect.ID3D10EffectVariable.AsRenderTargetView
title: ID3D10EffectVariable::AsRenderTargetView
author: windows-sdk-content
description: Get a render-target-view variable.
old-location: direct3d10\id3d10effectvariable_asrendertargetview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asrendertargetview.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 4e1e798b-0790-d8d7-5dc5-8b7d7e7de483, AsRenderTargetView, AsRenderTargetView method [Direct3D 10], AsRenderTargetView method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsRenderTargetView method, ID3D10EffectVariable.AsRenderTargetView, ID3D10EffectVariable::AsRenderTargetView, d3d10effect/ID3D10EffectVariable::AsRenderTargetView, direct3d10.id3d10effectvariable_asrendertargetview
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
 - ID3D10EffectVariable.AsRenderTargetView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectVariable::AsRenderTargetView


## -description


Get a render-target-view variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/71f158ed-9e0f-464c-b30f-4f8958d3f1a1">ID3D10EffectRenderTargetViewVariable</a>*</b>

A pointer to a render-target-view variable. See <a href="https://msdn.microsoft.com/71f158ed-9e0f-464c-b30f-4f8958d3f1a1">ID3D10EffectRenderTargetViewVariable Interface</a>.




## -remarks



This method returns a version of the effect variable that has been specialized to a render-target-view variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain render-target-view data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/b27f1669-94a1-4971-bd8f-e5a56f43560f">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>
 

 

