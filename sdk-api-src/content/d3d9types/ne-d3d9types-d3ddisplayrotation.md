---
UID: NE:d3d9types.D3DDISPLAYROTATION
title: D3DDISPLAYROTATION
author: windows-driver-content
description: Specifies how the monitor being used to display a full-screen application is rotated.
old-location: direct3d9\D3DDISPLAYROTATION.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddisplayrotation.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DDISPLAYROTATION, D3DDISPLAYROTATION enumeration [Direct3D 9], D3DDISPLAYROTATION_180, D3DDISPLAYROTATION_270, D3DDISPLAYROTATION_90, D3DDISPLAYROTATION_IDENTITY, d3d9types/D3DDISPLAYROTATION, d3d9types/D3DDISPLAYROTATION_180, d3d9types/D3DDISPLAYROTATION_270, d3d9types/D3DDISPLAYROTATION_90, d3d9types/D3DDISPLAYROTATION_IDENTITY, direct3d9.D3DDISPLAYROTATION, e726c4c1-db67-e754-9022-1e252bc25f14
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: D3DDISPLAYROTATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DDISPLAYROTATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3DDISPLAYROTATION enumeration


## -description


Specifies how the monitor being used to display a full-screen application is rotated.


## -enum-fields




### -field D3DDISPLAYROTATION_IDENTITY

Display is not rotated.


### -field D3DDISPLAYROTATION_90

Display is rotated 90 degrees.


### -field D3DDISPLAYROTATION_180

Display is rotated 180 degrees.


### -field D3DDISPLAYROTATION_270

Display is rotated 270 degrees.


## -remarks



This enumeration is used in <a href="https://msdn.microsoft.com/9c083fc7-85cf-4ea0-bb14-ee652231eb42">IDirect3D9Ex::GetAdapterDisplayModeEx</a>, <a href="https://msdn.microsoft.com/fa5b08f7-abb0-4f59-8454-4016cb029f1e">IDirect3DDevice9Ex::GetDisplayModeEx</a>, and <a href="https://msdn.microsoft.com/e0e37c67-941c-4153-8b69-edf2d640b96d">IDirect3DSwapChain9Ex::GetDisplayModeEx</a>.

Applications may choose to handle monitor rotation themselves by using the <a href="https://msdn.microsoft.com/1294171e-b3f6-4264-8411-b69427cefe7b">D3DPRESENTFLAG_NOAUTOROTATE</a>, in which case, the application will need to know how the monitor is rotated so that it may adjust its rendering accordingly.




## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

