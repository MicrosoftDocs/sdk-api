---
UID: NF:d2d1_3.ID2D1SvgGlyphStyle.GetStroke
title: ID2D1SvgGlyphStyle::GetStroke (d2d1_3.h)
author: windows-sdk-content
description: Returns the requested stroke parameters.
old-location: direct2d\id2d1svgglyphstyle_getstroke.htm
tech.root: Direct2D
ms.assetid: 5EC78516-E0E2-4758-9C36-47F951D1BCAE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStroke, GetStroke method [Direct2D], GetStroke method [Direct2D],ID2D1SvgGlyphStyle interface, ID2D1SvgGlyphStyle interface [Direct2D],GetStroke method, ID2D1SvgGlyphStyle.GetStroke, ID2D1SvgGlyphStyle::GetStroke, d2d1_3/ID2D1SvgGlyphStyle::GetStroke, direct2d.id2d1svgglyphstyle_getstroke
ms.topic: method
req.header: d2d1_3.h
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1SvgGlyphStyle.GetStroke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SvgGlyphStyle::GetStroke


## -description


Returns the requested stroke parameters. Any parameters that are non-null will receive the value of the requested parameter.
      


## -parameters




### -param brush [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>**</b>

Describes how the stroke is painted.


### -param strokeWidth [out, optional]

Type: <b>FLOAT*</b>

The 'context-value' for the 'stroke-width' property.


### -param dashes [out, optional]

Type: <b>FLOAT*</b>

The 'context-value' for the 'stroke-dasharray'
          property.


### -param dashesCount

Type: <b>UINT32</b>

The the number of dashes in the dash array.


### -param dashOffset [out, optional]

Type: <b>FLOAT*</b>

The 'context-value' for the 'stroke-dashoffset' property.


## -returns



This method does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1svgglyphstyle">ID2D1SvgGlyphStyle</a>
 

 

