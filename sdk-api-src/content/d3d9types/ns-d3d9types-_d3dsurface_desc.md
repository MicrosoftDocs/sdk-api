---
UID: NS:d3d9types._D3DSURFACE_DESC
title: "_D3DSURFACE_DESC"
author: windows-driver-content
description: Describes a surface.
old-location: direct3d9\d3dsurface_desc.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dsurface_desc.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 57ba605f-d20e-74e1-0a75-028f73419b59, D3DSURFACE_DESC, D3DSURFACE_DESC structure [Direct3D 9], LPD3DSURFACE_DESC, LPD3DSURFACE_DESC structure pointer [Direct3D 9], _D3DSURFACE_DESC, d3d9types/D3DSURFACE_DESC, d3d9types/LPD3DSURFACE_DESC, direct3d9.d3dsurface_desc
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
req.typenames: D3DSURFACE_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DSURFACE_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DSURFACE_DESC structure


## -description


Describes a surface.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, describing the surface format. 


### -field Type

Type: <b><a href="https://msdn.microsoft.com/6b360fb1-4a5a-47a2-bef9-d8234770bf0c">D3DRESOURCETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/6b360fb1-4a5a-47a2-bef9-d8234770bf0c">D3DRESOURCETYPE</a> enumerated type, identifying this resource as a surface. 


### -field Usage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Either the D3DUSAGE_DEPTHSTENCIL or D3DUSAGE_RENDERTARGET values. For more information, see <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a>.


### -field Pool

Type: <b><a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a></b>

Member of the <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a> enumerated type, specifying the class of memory allocated for this surface.


### -field MultiSampleType

Type: <b><a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a> enumerated type, specifying the levels of full-scene multisampling supported by the surface.


### -field MultiSampleQuality

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Quality level. The valid range is between zero and one less than the level returned by pQualityLevels used by  <a href="https://msdn.microsoft.com/82f1f1f6-0d9b-497b-b532-0d2aabbd0314">CheckDeviceMultiSampleType</a>. Passing a larger value returns the error, D3DERR_INVALIDCALL. The MultisampleQuality values of paired render targets, depth stencil surfaces and the MultiSample type must all match.


### -field Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the surface, in pixels.


### -field Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of the surface, in pixels.


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/b3fd1d5c-fb82-4f0d-a8af-ea181456079c">GetDesc</a>



<a href="https://msdn.microsoft.com/df5758fe-afb8-4821-92f1-53b8022b0e8e">GetLevelDesc</a>
 

 

