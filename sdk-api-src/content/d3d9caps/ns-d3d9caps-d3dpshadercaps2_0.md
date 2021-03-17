---
UID: NS:d3d9caps._D3DPSHADERCAPS2_0
title: D3DPSHADERCAPS2_0 (d3d9caps.h)
description: Pixel shader driver caps.
helpviewer_keywords: ["469d4061-0c45-7081-5150-edc65b416901","D3DPSHADERCAPS2_0","D3DPSHADERCAPS2_0 structure [Direct3D 9]","LPD3DPSHADERCAPS2_0","LPD3DPSHADERCAPS2_0 structure pointer [Direct3D 9]","d3d9caps/D3DPSHADERCAPS2_0","d3d9caps/LPD3DPSHADERCAPS2_0","direct3d9.d3dpshadercaps2_0"]
old-location: direct3d9\d3dpshadercaps2_0.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\d3dpshadercaps2_0.htm
ms.date: 12/05/2018
ms.keywords: 469d4061-0c45-7081-5150-edc65b416901, D3DPSHADERCAPS2_0, D3DPSHADERCAPS2_0 structure [Direct3D 9], LPD3DPSHADERCAPS2_0, LPD3DPSHADERCAPS2_0 structure pointer [Direct3D 9], d3d9caps/D3DPSHADERCAPS2_0, d3d9caps/LPD3DPSHADERCAPS2_0, direct3d9.d3dpshadercaps2_0
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
targetos: Windows
req.typenames: D3DPSHADERCAPS2_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3DPSHADERCAPS2_0
 - d3d9caps/_D3DPSHADERCAPS2_0
 - D3DPSHADERCAPS2_0
 - d3d9caps/D3DPSHADERCAPS2_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D9Caps.h
api_name:
 - D3DPSHADERCAPS2_0
---

# D3DPSHADERCAPS2_0 structure


## -description

Pixel shader driver caps.

## -struct-fields

### -field Caps

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Instruction predication is supported if this value is nonzero. See <a href="/windows/desktop/direct3dhlsl/setp-comp---vs">setp_comp - vs</a>.

### -field DynamicFlowControlDepth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Either 0 or 24, which represents the depth of the dynamic flow control instruction nesting. See <b>D3DPSHADERCAPS2_0</b>.

### -field NumTemps

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

The number of temporary registers supported. See <b>D3DPSHADERCAPS2_0</b>.

### -field StaticFlowControlDepth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

The depth of nesting of the <a href="/windows/desktop/direct3dhlsl/loop---vs">loop - vs</a>/<a href="/windows/desktop/direct3dhlsl/rep---vs">rep - vs</a> and <a href="/windows/desktop/direct3dhlsl/call---vs">call - vs</a>/<a href="/windows/desktop/direct3dhlsl/callnz-bool---vs">callnz bool - vs</a> instructions. See <b>D3DPSHADERCAPS2_0</b>.

### -field NumInstructionSlots

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

The number of instruction slots supported. See <b>D3DPSHADERCAPS2_0</b>.

## -see-also

<a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a>



<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-structures">Direct3D Structures</a>