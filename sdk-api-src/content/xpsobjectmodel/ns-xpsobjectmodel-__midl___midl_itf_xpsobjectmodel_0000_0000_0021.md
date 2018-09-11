---
UID: NS:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0021
title: "__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0021"
author: windows-sdk-content
description: Describes the placement and location of a glyph.
old-location: xps\xps_glyph_index.htm
tech.root: printdocs
ms.assetid: 0ea30e0f-f32b-4a38-9591-27cb1fe7f234
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: XPS_GLYPH_INDEX, XPS_GLYPH_INDEX structure [XPS Documents and Packaging], __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0021, xps.xps_glyph_index, xpsobjectmodel/XPS_GLYPH_INDEX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - xpsobjectmodel.h
api_name:
 - XPS_GLYPH_INDEX
product: Windows
targetos: Windows
req.typenames: XPS_GLYPH_INDEX
req.redist: 
---

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0021 structure


## -description


Describes the placement and location of a glyph.


## -struct-fields




### -field index

The index of a glyph in the physical font.


### -field advanceWidth

Indicates the  placement of the glyph that follows,  relative to the origin of the current glyph. Measured in hundredths of the font's em-size.


### -field horizontalOffset

The horizontal distance, in the effective coordinate space, by which to move the glyph from the glyph's origin. Measured in hundredths of the font's em-size.


### -field verticalOffset

The vertical distance, in the effective coordinate space, by which to move the glyph from the glyph's origin. Measured in hundredths of the font's  em-size.


## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

