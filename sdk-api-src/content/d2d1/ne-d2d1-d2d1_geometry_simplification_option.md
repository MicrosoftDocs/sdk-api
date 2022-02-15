---
UID: NE:d2d1.D2D1_GEOMETRY_SIMPLIFICATION_OPTION
title: D2D1_GEOMETRY_SIMPLIFICATION_OPTION (d2d1.h)
description: Specifies how a geometry is simplified to an ID2D1SimplifiedGeometrySink.
helpviewer_keywords: ["D2D1_GEOMETRY_SIMPLIFICATION_OPTION","D2D1_GEOMETRY_SIMPLIFICATION_OPTION enumeration [Direct2D]","D2D1_GEOMETRY_SIMPLIFICATION_OPTION_CUBICS_AND_LINES","D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES","d2d1/D2D1_GEOMETRY_SIMPLIFICATION_OPTION","d2d1/D2D1_GEOMETRY_SIMPLIFICATION_OPTION_CUBICS_AND_LINES","d2d1/D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES","direct2d.D2D1_GEOMETRY_SIMPLIFICATION_OPTION"]
old-location: direct2d\D2D1_GEOMETRY_SIMPLIFICATION_OPTION.htm
tech.root: Direct2D
ms.assetid: cda5968b-843b-4759-ae0f-cb83e9990590
ms.date: 12/05/2018
ms.keywords: D2D1_GEOMETRY_SIMPLIFICATION_OPTION, D2D1_GEOMETRY_SIMPLIFICATION_OPTION enumeration [Direct2D], D2D1_GEOMETRY_SIMPLIFICATION_OPTION_CUBICS_AND_LINES, D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES, d2d1/D2D1_GEOMETRY_SIMPLIFICATION_OPTION, d2d1/D2D1_GEOMETRY_SIMPLIFICATION_OPTION_CUBICS_AND_LINES, d2d1/D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES, direct2d.D2D1_GEOMETRY_SIMPLIFICATION_OPTION
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
req.typenames: D2D1_GEOMETRY_SIMPLIFICATION_OPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_GEOMETRY_SIMPLIFICATION_OPTION
 - d2d1/D2D1_GEOMETRY_SIMPLIFICATION_OPTION
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
 - D2D1_GEOMETRY_SIMPLIFICATION_OPTION
---

# D2D1_GEOMETRY_SIMPLIFICATION_OPTION enumeration


## -description

Specifies how a geometry is simplified to an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>.

## -enum-fields

### -field D2D1_GEOMETRY_SIMPLIFICATION_OPTION_CUBICS_AND_LINES:0

The output can contain cubic Bezier curves and line segments.

### -field D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES:1

The output is flattened so that it contains only line segments.

### -field D2D1_GEOMETRY_SIMPLIFICATION_OPTION_FORCE_DWORD:0xffffffff

## -see-also

<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-simplify(d2d1_geometry_simplification_option_constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink)">ID2D1Geometry::Simplify</a>

