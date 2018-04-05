---
UID: NS:d3d9types._D3DVOLUME_DESC
title: "_D3DVOLUME_DESC"
author: windows-driver-content
description: Describes a volume.
old-location: direct3d9\d3dvolume_desc.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dvolume_desc.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DVOLUME_DESC, D3DVOLUME_DESC structure [Direct3D 9], LPD3DVOLUME_DESC, LPD3DVOLUME_DESC structure pointer [Direct3D 9], _D3DVOLUME_DESC, d3d9types/D3DVOLUME_DESC, d3d9types/LPD3DVOLUME_DESC, direct3d9.d3dvolume_desc, e489902a-8c89-f2e8-5f2a-7f9eb32316cb
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
req.typenames: D3DVOLUME_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DVOLUME_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DVOLUME_DESC structure


## -description


Describes a volume.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, describing the surface format of the volume. 


### -field Type

Type: <b><a href="https://msdn.microsoft.com/6b360fb1-4a5a-47a2-bef9-d8234770bf0c">D3DRESOURCETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/6b360fb1-4a5a-47a2-bef9-d8234770bf0c">D3DRESOURCETYPE</a> enumerated type, identifying this resource as a volume. 


### -field Usage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Currently not used. Always returned as 0. 


### -field Pool

Type: <b><a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a></b>

Member of the <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a> enumerated type, specifying the class of memory allocated for this volume. 


### -field Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the volume, in pixels. 


### -field Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of the volume, in pixels. 


### -field Depth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Depth of the volume, in pixels. 


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/7b3f60c3-9bb6-45d3-aa57-148b7089bf15">GetDesc</a>



<a href="https://msdn.microsoft.com/6d8db22a-6903-4693-a991-2b8dde32bc35">GetLevelDesc</a>
 

 

