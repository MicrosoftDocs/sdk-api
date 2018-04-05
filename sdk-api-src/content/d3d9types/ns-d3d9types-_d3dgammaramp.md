---
UID: NS:d3d9types._D3DGAMMARAMP
title: "_D3DGAMMARAMP"
author: windows-driver-content
description: Contains red, green, and blue ramp data.
old-location: direct3d9\d3dgammaramp.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dgammaramp.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DGAMMARAMP, D3DGAMMARAMP structure [Direct3D 9], LPD3DGAMMARAMP, LPD3DGAMMARAMP structure pointer [Direct3D 9], _D3DGAMMARAMP, a47af298-5e94-f2c5-0c7e-5867734bf434, d3d9types/D3DGAMMARAMP, d3d9types/LPD3DGAMMARAMP, direct3d9.d3dgammaramp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
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
req.typenames: D3DGAMMARAMP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DGAMMARAMP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DGAMMARAMP structure


## -description


Contains red, green, and blue ramp data.


## -struct-fields




### -field red

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Array of 256 
    WORD element that describes the red gamma ramp. 


### -field green

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Array of 256 
    WORD element that describes the green gamma ramp. 


### -field blue

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Array of 256 
    WORD element that describes the blue gamma ramp. 


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/798ed6ed-ae8b-412d-b70b-024d198eb16f">GetGammaRamp</a>



<a href="https://msdn.microsoft.com/ad44b71a-f391-49bb-963d-705f6dd9325c">SetGammaRamp</a>
 

 

