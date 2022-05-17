---
UID: NF:d2d1helper.ColorF.ColorF(FLOAT,FLOAT,FLOAT,FLOAT)
title: ColorF::ColorF(FLOAT,FLOAT,FLOAT,FLOAT) (d2d1helper.h)
description: Instantiates a new instance of the ColorF class that contains the specified red, green, blue, and alpha values.
helpviewer_keywords: ["ColorF","ColorF interface [Direct2D]","ColorF(FLOAT","FLOAT","FLOAT","FLOAT) constructor","ColorF(FLOAT","FLOAT","FLOAT","FLOAT) constructor [Direct2D]","ColorF(FLOAT","FLOAT","FLOAT","FLOAT) constructor [Direct2D]","ColorF interface","ColorF.ColorF","ColorF.ColorF(FLOAT","FLOAT","FLOAT","FLOAT)","ColorF::ColorF","ColorF::ColorF(FLOAT","FLOAT","FLOAT","FLOAT)","ColorF::ColorF(FLOAT","FLOAT","FLOAT","FLOAT)(FLOAT","FLOAT","FLOAT","FLOAT)","D2D1.ColorF.ColorF(FLOAT","FLOAT","FLOAT","FLOAT)","D2D1::ColorF::ColorF(FLOAT","FLOAT","FLOAT","FLOAT)","d2d1helper/ColorF::ColorF(FLOAT","FLOAT","FLOAT","FLOAT)","direct2d.colorf_colorf_float__float__float__float_"]
old-location: direct2d\colorf_colorf_float__float__float__float_.htm
tech.root: Direct2D
ms.assetid: 0c6118e6-0d97-4f66-951a-01e6d5264c59
ms.date: 12/05/2018
ms.keywords: ColorF, ColorF interface [Direct2D],ColorF(FLOAT,FLOAT,FLOAT,FLOAT) constructor, ColorF(FLOAT,FLOAT,FLOAT,FLOAT) constructor [Direct2D], ColorF(FLOAT,FLOAT,FLOAT,FLOAT) constructor [Direct2D],ColorF interface, ColorF.ColorF, ColorF.ColorF(FLOAT,FLOAT,FLOAT,FLOAT), ColorF::ColorF, ColorF::ColorF(FLOAT,FLOAT,FLOAT,FLOAT), ColorF::ColorF(FLOAT,FLOAT,FLOAT,FLOAT)(FLOAT,FLOAT,FLOAT,FLOAT), D2D1.ColorF.ColorF(FLOAT,FLOAT,FLOAT,FLOAT), D2D1::ColorF::ColorF(FLOAT,FLOAT,FLOAT,FLOAT), d2d1helper/ColorF::ColorF(FLOAT,FLOAT,FLOAT,FLOAT), direct2d.colorf_colorf_float__float__float__float_
req.header: d2d1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: D2D1
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ColorF::ColorF
 - d2d1helper/ColorF::ColorF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ColorF.ColorF(FLOAT, FLOAT, FLOAT, FLOAT)
---

# ColorF::ColorF(FLOAT,FLOAT,FLOAT,FLOAT)


## -description

Instantiates a new instance of the <a href="/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf">ColorF</a> class that contains the specified red, green, blue, and alpha values.

## -parameters

### -param red

Type: <b>FLOAT</b>

The red component of the color to be constructed.

### -param green

Type: <b>FLOAT</b>

The green component of the color to be constructed.

### -param blue

Type: <b>FLOAT</b>

The blue component of the color to be constructed.

### -param alpha

Type: <b>FLOAT</b>

The alpha value of the color to be constructed. An alpha channel value ranges from 0.0 to 1.0, where 0.0 represents a fully transparent color and 1.0  represents a fully opaque color. This argument is optional and if omitted will default to 1.0 (Fully opaque).

## -see-also

<a href="/windows/desktop/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf">ColorF</a>
