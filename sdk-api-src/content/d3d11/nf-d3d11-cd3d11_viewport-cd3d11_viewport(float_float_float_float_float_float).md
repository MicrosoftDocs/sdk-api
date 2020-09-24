---
UID: NF:d3d11.CD3D11_VIEWPORT.CD3D11_VIEWPORT(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)
title: CD3D11_VIEWPORT::CD3D11_VIEWPORT(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT) (d3d11.h)
description: Instantiates a new instance of a CD3D11_VIEWPORT structure that is initialized with D3D11_VIEWPORT values.
helpviewer_keywords: ["CD3D11_VIEWPORT","CD3D11_VIEWPORT constructor [Direct3D 11]","CD3D11_VIEWPORT constructor [Direct3D 11]","CD3D11_VIEWPORT interface","CD3D11_VIEWPORT interface [Direct3D 11]","CD3D11_VIEWPORT constructor","CD3D11_VIEWPORT.CD3D11_VIEWPORT","CD3D11_VIEWPORT.CD3D11_VIEWPORT(FLOAT","FLOAT","FLOAT","FLOAT","FLOAT","FLOAT)","CD3D11_VIEWPORT::CD3D11_VIEWPORT","CD3D11_VIEWPORT::CD3D11_VIEWPORT(FLOAT","FLOAT","FLOAT","FLOAT","FLOAT","FLOAT)","d3d11/CD3D11_VIEWPORT::CD3D11_VIEWPORT","direct3d11.cd3d11_viewport_cd3d11_viewport_d3d11_viewport_values_"]
old-location: direct3d11\cd3d11_viewport_cd3d11_viewport_d3d11_viewport_values_.htm
tech.root: direct3d11
ms.assetid: EDC5768A-0BF4-40B4-ABDC-67701A75FB8A
ms.date: 12/05/2018
ms.keywords: CD3D11_VIEWPORT, CD3D11_VIEWPORT constructor [Direct3D 11], CD3D11_VIEWPORT constructor [Direct3D 11],CD3D11_VIEWPORT interface, CD3D11_VIEWPORT interface [Direct3D 11],CD3D11_VIEWPORT constructor, CD3D11_VIEWPORT.CD3D11_VIEWPORT, CD3D11_VIEWPORT.CD3D11_VIEWPORT(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT), CD3D11_VIEWPORT::CD3D11_VIEWPORT, CD3D11_VIEWPORT::CD3D11_VIEWPORT(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT), d3d11/CD3D11_VIEWPORT::CD3D11_VIEWPORT, direct3d11.cd3d11_viewport_cd3d11_viewport_d3d11_viewport_values_
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CD3D11_VIEWPORT::CD3D11_VIEWPORT
 - d3d11/CD3D11_VIEWPORT::CD3D11_VIEWPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - CD3D11_VIEWPORT.CD3D11_VIEWPORT
---

# CD3D11_VIEWPORT::CD3D11_VIEWPORT(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)


## -description

Instantiates a new instance of a <a href="/previous-versions/windows/desktop/legacy/jj151722(v=vs.85)">CD3D11_VIEWPORT</a> structure that is initialized with <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_viewport">D3D11_VIEWPORT</a> values.

## -parameters

### -param topLeftX

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

X position of the left hand side of the viewport. Ranges between D3D11_VIEWPORT_BOUNDS_MIN and D3D11_VIEWPORT_BOUNDS_MAX.

### -param topLeftY

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Y position of the top of the viewport. Ranges between D3D11_VIEWPORT_BOUNDS_MIN and D3D11_VIEWPORT_BOUNDS_MAX.

### -param width

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Width of the viewport.

### -param height

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Height of the viewport.

### -param minDepth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Minimum depth of the viewport. Ranges between 0 and 1.

### -param maxDepth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Maximum depth of the viewport. Ranges between 0 and 1.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/jj151722(v=vs.85)">CD3D11_VIEWPORT</a>