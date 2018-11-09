---
UID: NS:d3d9caps._D3DPSHADERCAPS2_0
title: "_D3DPSHADERCAPS2_0"
author: windows-sdk-content
description: Pixel shader driver caps.
old-location: direct3d9\d3dpshadercaps2_0.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\d3dpshadercaps2_0.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 469d4061-0c45-7081-5150-edc65b416901, D3DPSHADERCAPS2_0, D3DPSHADERCAPS2_0 structure [Direct3D 9], LPD3DPSHADERCAPS2_0, LPD3DPSHADERCAPS2_0 structure pointer [Direct3D 9], _D3DPSHADERCAPS2_0, d3d9caps/D3DPSHADERCAPS2_0, d3d9caps/LPD3DPSHADERCAPS2_0, direct3d9.d3dpshadercaps2_0
ms.prod: windows
ms.technology: windows-sdk
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
 - D3DPSHADERCAPS2_0
product: Windows
targetos: Windows
req.typenames: D3DPSHADERCAPS2_0
req.redist: 
---

# _D3DPSHADERCAPS2_0 structure


## -description


Pixel shader driver caps.


## -struct-fields




### -field Caps

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Instruction predication is supported if this value is nonzero. See <a href="https://msdn.microsoft.com/en-us/library/Bb147357(v=VS.85).aspx">setp_comp - vs</a>.


### -field DynamicFlowControlDepth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Either 0 or 24, which represents the depth of the dynamic flow control instruction nesting. See <b>D3DPSHADERCAPS2_0</b>.


### -field NumTemps

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The number of temporary registers supported. See <b>D3DPSHADERCAPS2_0</b>.


### -field StaticFlowControlDepth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The depth of nesting of the <a href="https://msdn.microsoft.com/en-us/library/Bb174716(v=VS.85).aspx">loop - vs</a>/<a href="https://msdn.microsoft.com/en-us/library/Bb147331(v=VS.85).aspx">rep - vs</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb172389(v=VS.85).aspx">call - vs</a>/<a href="https://msdn.microsoft.com/en-us/library/Bb172385(v=VS.85).aspx">callnz bool - vs</a> instructions. See <b>D3DPSHADERCAPS2_0</b>.


### -field NumInstructionSlots

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The number of instruction slots supported. See <b>D3DPSHADERCAPS2_0</b>.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a>



<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

