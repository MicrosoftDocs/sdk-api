---
UID: NF:d3d10effect.ID3D10Effect.GetDesc
title: ID3D10Effect::GetDesc method
author: windows-driver-content
description: Get an effect description.
old-location: direct3d10\id3d10effect_getdesc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getdesc.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 35c1c99a-3f41-0efe-adae-ce9709830b32, GetDesc method [Direct3D 10], GetDesc method [Direct3D 10], ID3D10Effect interface, GetDesc,ID3D10Effect.GetDesc, ID3D10Effect, ID3D10Effect interface [Direct3D 10], GetDesc method, ID3D10Effect::GetDesc, d3d10effect/ID3D10Effect::GetDesc, direct3d10.id3d10effect_getdesc
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10Effect.h
api_name:
-	ID3D10Effect.GetDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Effect::GetDesc method


## -description


Get an effect description.


## -parameters




### -param pDesc [in, out]

Type: <b><a href="https://msdn.microsoft.com/4e25e0d5-b614-4dba-ade2-e60b468c46a4">D3D10_EFFECT_DESC</a>*</b>

A pointer to an effect description (see <a href="https://msdn.microsoft.com/4e25e0d5-b614-4dba-ade2-e60b468c46a4">D3D10_EFFECT_DESC</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



An effect description contains basic information about an effect such as the techniques it contains and the constant buffer resources it requires.




## -see-also




<a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect Interface</a>
 

 

