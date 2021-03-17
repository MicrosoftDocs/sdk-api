---
UID: NS:dxgicommon.DXGI_RATIONAL
title: DXGI_RATIONAL (dxgicommon.h)
description: Represents a rational number.
helpviewer_keywords: ["5deaf109-e4cc-0f12-82f4-0d4d0b2e387a","DXGI_RATIONAL","DXGI_RATIONAL structure [DXGI]","direct3ddxgi.dxgi_rational","dxgicommon/DXGI_RATIONAL"]
old-location: direct3ddxgi\dxgi_rational.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_rational.htm
ms.date: 12/05/2018
ms.keywords: 5deaf109-e4cc-0f12-82f4-0d4d0b2e387a, DXGI_RATIONAL, DXGI_RATIONAL structure [DXGI], direct3ddxgi.dxgi_rational, dxgicommon/DXGI_RATIONAL
req.header: dxgicommon.h
req.include-header: DXGI.h
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
req.typenames: DXGI_RATIONAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_RATIONAL
 - dxgicommon/DXGI_RATIONAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgicommon.h
api_name:
 - DXGI_RATIONAL
---

# DXGI_RATIONAL structure


## -description

Represents a rational number.

## -struct-fields

### -field Numerator

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An unsigned integer value representing the top of the rational number.

### -field Denominator

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An unsigned integer value representing the bottom of the rational number.

## -remarks

This structure is a member of the <a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a> structure.

The <b>DXGI_RATIONAL</b> structure operates under the following rules:

<ul>
<li>0/0 is legal and will be interpreted as 0/1.</li>
<li>0/anything is interpreted as zero.</li>
<li>If you are representing a whole number, the denominator should be 1.</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>