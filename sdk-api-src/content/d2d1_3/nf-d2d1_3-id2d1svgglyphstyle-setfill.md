---
UID: NF:d2d1_3.ID2D1SvgGlyphStyle.SetFill
title: ID2D1SvgGlyphStyle::SetFill
author: windows-sdk-content
description: Provides values to an SVG glyph for fill.
old-location: direct2d\id2d1svgglyphstyle_setfill.htm
tech.root: direct2d
ms.assetid: 7F8D423C-6A3A-4240-87E9-515F5FE29C1D
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID2D1SvgGlyphStyle interface [Direct2D],SetFill method, ID2D1SvgGlyphStyle.SetFill, ID2D1SvgGlyphStyle::SetFill, SetFill, SetFill method [Direct2D], SetFill method [Direct2D],ID2D1SvgGlyphStyle interface, d2d1_3/ID2D1SvgGlyphStyle::SetFill, direct2d.id2d1svgglyphstyle_setfill
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1SvgGlyphStyle.SetFill
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgGlyphStyle::SetFill


## -description


Provides values to an SVG glyph for fill.


## -parameters




### -param brush [in, optional]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

Describes how the area is painted.  A null brush will cause the context-fill value to come from
          the <a href="https://msdn.microsoft.com/1B7DA239-9788-44E9-86A8-205E8CCDD065">defaultFillBrush</a>. If the defaultFillBrush is also null, the context-fill value will be 'none'.
          To set the ‘context-fill’ value, this method uses the provided brush with its opacity set to 1. To set the ‘context-fill-opacity’ value, this method uses the opacity of the provided brush.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/FE01771A-D82A-4610-8014-E0C0C0C5402E">ID2D1SvgGlyphStyle</a>
 

 

