---
UID: NS:d3d9caps._D3DVSHADERCAPS2_0
title: D3DVSHADERCAPS2_0 (d3d9caps.h)
author: windows-sdk-content
description: Vertex shader caps.
old-location: direct3d9\d3dvshadercaps2_0.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\d3dvshadercaps2_0.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 85a71d10-ae0f-bdc3-e929-6d1ff3c0b356, D3DVSHADERCAPS2_0, D3DVSHADERCAPS2_0 structure [Direct3D 9], LPD3DVSHADERCAPS2_0, LPD3DVSHADERCAPS2_0 structure pointer [Direct3D 9], d3d9caps/D3DVSHADERCAPS2_0, d3d9caps/LPD3DVSHADERCAPS2_0, direct3d9.d3dvshadercaps2_0
ms.topic: struct
req.header: d3d9caps.h
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
 - HeaderDef
api_location:
 - D3D9Caps.h
api_name:
 - D3DVSHADERCAPS2_0
product: Windows
targetos: Windows
req.typenames: D3DVSHADERCAPS2_0
req.redist: 
ms.custom: 19H1
---

# D3DVSHADERCAPS2_0 structure


## -description


Vertex shader caps.


## -struct-fields




### -field Caps

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Instruction predication is supported if this value is nonzero. See <a href="https://msdn.microsoft.com/en-us/library/Bb147357(v=VS.85).aspx">setp_comp - vs</a>.


### -field DynamicFlowControlDepth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

 Either 0 or 24, which represents the depth of the dynamic flow control instruction nesting. See <a href="https://msdn.microsoft.com/en-us/library/Bb172634(v=VS.85).aspx">D3DVS20CAPS</a>.


### -field NumTemps

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The number of temporary registers supported. See <a href="https://msdn.microsoft.com/en-us/library/Bb172634(v=VS.85).aspx">D3DVS20CAPS</a>.


### -field StaticFlowControlDepth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The depth of nesting of the <a href="https://msdn.microsoft.com/en-us/library/Bb174716(v=VS.85).aspx">loop - vs</a>/<a href="https://msdn.microsoft.com/en-us/library/Bb147331(v=VS.85).aspx">rep - vs</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb172389(v=VS.85).aspx">call - vs</a>/<a href="https://msdn.microsoft.com/en-us/library/Bb172385(v=VS.85).aspx">callnz bool - vs</a> instructions. See <a href="https://msdn.microsoft.com/en-us/library/Bb172634(v=VS.85).aspx">D3DVS20CAPS</a>.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172591(v=VS.85).aspx">D3DPSHADERCAPS2_0</a>



<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

