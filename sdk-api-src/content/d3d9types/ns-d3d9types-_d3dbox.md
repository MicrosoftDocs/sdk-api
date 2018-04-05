---
UID: NS:d3d9types._D3DBOX
title: "_D3DBOX"
author: windows-driver-content
description: Defines a volume.
old-location: direct3d9\d3dbox.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dbox.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DBOX, D3DBOX structure [Direct3D 9], LPD3DBOX, LPD3DBOX structure pointer [Direct3D 9], _D3DBOX, d3d9types/D3DBOX, d3d9types/LPD3DBOX, dd4d6877-d9c7-7afc-b142-136d810a5600, direct3d9.d3dbox
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
req.typenames: D3DBOX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DBOX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DBOX structure


## -description


Defines a volume.


## -struct-fields




### -field Left

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Position of the left side of the box on the x-axis.


### -field Top

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Position of the top of the box on the y-axis.


### -field Right

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Position of the right side of the box on the x-axis.


### -field Bottom

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Position of the bottom of the box on the y-axis.


### -field Front

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Position of the front of the box on the z-axis.


### -field Back

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Position of the back of the box on the z-axis.


## -remarks



<b>D3DBOX</b> includes the left, top, and front edges; however, the right, bottom, and back edges are not included. For example, a box that is 100 units wide and begins at 0 (thus, including the points up to and including 99) would be expressed with a value of 0 for the Left member and a value of 100 for the Right member. Note that a value of 99 is not used for the Right member.

The restrictions on side ordering observed for <b>D3DBOX</b> are left to right, top to bottom, and front to back.




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

