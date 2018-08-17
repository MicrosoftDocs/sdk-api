---
UID: NC:winddi.PFN_DrvQueryGlyphAttrs
title: PFN_DrvQueryGlyphAttrs
author: windows-sdk-content
description: The DrvQueryGlyphAttrs function returns information about a font's glyphs.
old-location: display\drvqueryglyphattrs.htm
old-project: display
ms.assetid: cfc42384-581c-4358-84a9-91028c89bbd8
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: DrvQueryGlyphAttrs, DrvQueryGlyphAttrs callback, DrvQueryGlyphAttrs callback function [Display Devices], PFN_DrvQueryGlyphAttrs, ddifncs_9040dac6-091f-4400-99e2-ce91dd952494.xml, display.drvqueryglyphattrs, winddi/DrvQueryGlyphAttrs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
req.target-type: Desktop
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winddi.h
api_name:
 - DrvQueryGlyphAttrs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFN_DrvQueryGlyphAttrs callback function


## -description


The <b>DrvQueryGlyphAttrs</b> function returns information about a font's glyphs.


## -parameters




### -param *


### -param Arg1








#### - iMode [in]

GDI-supplied flag indicating the type of glyph attribute being requested. The following flag is defined:

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
FO_ATTR_MODE_ROTATE

</td>
<td>
The function returns an array indicating which glyphs of a vertical font must be rotated.

</td>
</tr>
</table>
 


#### - pfo [in]

GDI-supplied pointer to a <a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a> structure identifying the font for which attributes are being requested.


## -returns



<b>DrvQueryGlyphAttrs</b> should return a pointer to an <a href="https://msdn.microsoft.com/25a5c390-244c-4cff-a6a5-cc61fc5aa40b">FD_GLYPHATTR</a> structure. If an error is encountered, such as an invalid input argument, or if the font described by the <a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a> structure is not a vertical font, the function should return <b>NULL</b>.




## -remarks



The <b>DrvQueryGlyphAttrs</b> function should be supplied by font drivers. Currently, the only attribute flag defined is FO_ATTR_MODE_ROTATE, meaning the function should indicate which glyphs of a vertical font must be rotated. (For vertical fonts, DBCS glyphs must be rotated.) This information is useful to printer drivers that support printers having built-in font rasterizers.

The function should return rotation information in the <a href="https://msdn.microsoft.com/25a5c390-244c-4cff-a6a5-cc61fc5aa40b">FD_GLYPHATTR</a> structure that is used as the function's return value.

GDI calls the appropriate font driver's <b>DrvQueryGlyphAttrs</b> function when a printer driver calls GDI's <a href="https://msdn.microsoft.com/6a619922-5ab6-4169-8b41-e645e9d7fe93">FONTOBJ_pQueryGlyphAttrs</a> function.




## -see-also




<a href="https://msdn.microsoft.com/25a5c390-244c-4cff-a6a5-cc61fc5aa40b">FD_GLYPHATTR</a>



<a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a>



<a href="https://msdn.microsoft.com/6a619922-5ab6-4169-8b41-e645e9d7fe93">FONTOBJ_pQueryGlyphAttrs</a>
 

 

