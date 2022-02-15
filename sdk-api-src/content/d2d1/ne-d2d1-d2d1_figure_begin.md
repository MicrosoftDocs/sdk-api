---
UID: NE:d2d1.D2D1_FIGURE_BEGIN
title: D2D1_FIGURE_BEGIN (d2d1.h)
description: Indicates whether a specific ID2D1SimplifiedGeometrySink figure is filled or hollow.
helpviewer_keywords: ["D2D1_FIGURE_BEGIN","D2D1_FIGURE_BEGIN enumeration [Direct2D]","D2D1_FIGURE_BEGIN_FILLED","D2D1_FIGURE_BEGIN_HOLLOW","d2d1/D2D1_FIGURE_BEGIN","d2d1/D2D1_FIGURE_BEGIN_FILLED","d2d1/D2D1_FIGURE_BEGIN_HOLLOW","direct2d.D2D1_FIGURE_BEGIN"]
old-location: direct2d\D2D1_FIGURE_BEGIN.htm
tech.root: Direct2D
ms.assetid: c29aa79e-b978-4318-a8e1-5a321cd66327
ms.date: 12/05/2018
ms.keywords: D2D1_FIGURE_BEGIN, D2D1_FIGURE_BEGIN enumeration [Direct2D], D2D1_FIGURE_BEGIN_FILLED, D2D1_FIGURE_BEGIN_HOLLOW, d2d1/D2D1_FIGURE_BEGIN, d2d1/D2D1_FIGURE_BEGIN_FILLED, d2d1/D2D1_FIGURE_BEGIN_HOLLOW, direct2d.D2D1_FIGURE_BEGIN
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: D2D1_FIGURE_BEGIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_FIGURE_BEGIN
 - d2d1/D2D1_FIGURE_BEGIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_FIGURE_BEGIN
---

# D2D1_FIGURE_BEGIN enumeration


## -description

Indicates whether a specific <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a> figure is filled or hollow.

## -enum-fields

### -field D2D1_FIGURE_BEGIN_FILLED:0

Indicates the figure will be filled by the FillGeometry (<a href="/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillgeometry">ID2D1CommandSink::FillGeometry</a> 
          or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry">ID2D1RenderTarget::FillGeometry</a>) method.

### -field D2D1_FIGURE_BEGIN_HOLLOW:1

Indicates the figure will not be filled by the FillGeometry (<a href="/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillgeometry">ID2D1CommandSink::FillGeometry</a> 
          or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry">ID2D1RenderTarget::FillGeometry</a>) method and will only consist of an outline. 
          Moreover, the bounds of a hollow figure are zero. 
          D2D1_FIGURE_BEGIN_HOLLOW should be used for stroking, or for other geometry operations.

### -field D2D1_FIGURE_BEGIN_FORCE_DWORD:0xffffffff

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure">ID2D1SimplifiedGeometrySink::BeginFigure</a>



<a href="/windows/win32/Direct2D/path-geometries-overview">Path Geometries Overview</a>

