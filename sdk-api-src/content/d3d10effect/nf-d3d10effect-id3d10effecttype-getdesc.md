---
UID: NF:d3d10effect.ID3D10EffectType.GetDesc
title: ID3D10EffectType::GetDesc
author: windows-sdk-content
description: Get an effect-type description.
old-location: direct3d10\id3d10effecttype_getdesc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttype_getdesc.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 9e64bfa1-7fde-b141-e176-3bdc98f92982, GetDesc, GetDesc method [Direct3D 10], GetDesc method [Direct3D 10],ID3D10EffectType interface, ID3D10EffectType interface [Direct3D 10],GetDesc method, ID3D10EffectType.GetDesc, ID3D10EffectType::GetDesc, d3d10effect/ID3D10EffectType::GetDesc, direct3d10.id3d10effecttype_getdesc
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10Effect.h
api_name:
-	ID3D10EffectType.GetDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectType::GetDesc


## -description


Get an effect-type description.


## -parameters




### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/6ed4c32f-26f7-47c0-b8dc-6520364113e9">D3D10_EFFECT_TYPE_DESC</a>*</b>

A pointer to an effect-type description. See <a href="https://msdn.microsoft.com/6ed4c32f-26f7-47c0-b8dc-6520364113e9">D3D10_EFFECT_TYPE_DESC</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



The effect-variable description contains data about the name, annotations, semantic, flags and buffer offset of the effect type.




## -see-also




<a href="https://msdn.microsoft.com/8b396c86-82de-4a0e-8b86-228e3716c09b">ID3D10EffectType Interface</a>
 

 

