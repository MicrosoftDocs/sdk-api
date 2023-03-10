---
UID: NN:d2d1svg.ID2D1SvgPathData
title: ID2D1SvgPathData (d2d1svg.h)
description: Interface describing SVG path data. Path data can be set as the 'd' attribute on a 'path' element.
helpviewer_keywords: ["ID2D1SvgPathData","ID2D1SvgPathData interface [Direct2D]","ID2D1SvgPathData interface [Direct2D]","described","d2d1svg/ID2D1SvgPathData","direct2d.id2d1svgpathdata"]
old-location: direct2d\id2d1svgpathdata.htm
tech.root: Direct2D
ms.assetid: 14879B17-0CAA-42E7-8643-7D385EABFD37
ms.date: 12/05/2018
ms.keywords: ID2D1SvgPathData, ID2D1SvgPathData interface [Direct2D], ID2D1SvgPathData interface [Direct2D],described, d2d1svg/ID2D1SvgPathData, direct2d.id2d1svgpathdata
req.header: d2d1svg.h
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
req.dll: Direct2d.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1SvgPathData
 - d2d1svg/ID2D1SvgPathData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgPathData
---

# ID2D1SvgPathData interface


## -description

Interface describing SVG path data. Path data can be set as the 'd' attribute on a 'path' element.

The path data set is factored into two arrays. The segment data array stores all
        numbers and the commands array stores the set of commands. Unlike the string
        data set in the d attribute, each command in this representation uses a fixed
        number of elements in the segment data array. Therefore, the path 'M 0,0 100,0
        0,100 Z' is represented as: 'M0,0 L100,0 L0,100 Z'. This is split into two
        arrays, with the segment data containing '0,0 100,0 0,100', and the commands
        containing 'M L L Z'.

## -inheritance

The <b>ID2D1SvgPathData</b> interface inherits from <a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgattribute">ID2D1SvgAttribute</a>. <b>ID2D1SvgPathData</b> also has these types of members:

