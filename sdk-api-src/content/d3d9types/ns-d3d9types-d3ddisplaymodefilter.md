---
UID: NS:d3d9types.D3DDISPLAYMODEFILTER
title: D3DDISPLAYMODEFILTER
author: windows-driver-content
description: Specifies types of display modes to filter out.
old-location: direct3d9\d3ddisplaymodefilter.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddisplaymodefilter.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 7ce20661-a802-32fd-7091-b46cfddc1258, D3DDISPLAYMODEFILTER, D3DDISPLAYMODEFILTER structure [Direct3D 9], d3d9types/D3DDISPLAYMODEFILTER, direct3d9.d3ddisplaymodefilter
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
req.typenames: D3DDISPLAYMODEFILTER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DDISPLAYMODEFILTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3DDISPLAYMODEFILTER structure


## -description


Specifies types of display modes to filter out.


## -struct-fields




### -field Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size of this structure. This should always be set to sizeof(D3DDISPLAYMODEFILTER).


### -field Format

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

The display mode format to filter out. See <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>.


### -field ScanLineOrdering

Type: <b><a href="https://msdn.microsoft.com/55cf790e-ebe9-4791-a2be-a90fc76bae57">D3DSCANLINEORDERING</a></b>

Whether the scanline ordering is interlaced or progressive. See <a href="https://msdn.microsoft.com/55cf790e-ebe9-4791-a2be-a90fc76bae57">D3DSCANLINEORDERING</a>.


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

