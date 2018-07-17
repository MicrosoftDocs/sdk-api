---
UID: NF:winddi.STROBJ_bEnumPositionsOnly
title: STROBJ_bEnumPositionsOnly function
author: windows-sdk-content
description: The STROBJ_bEnumPositionsOnly function enumerates glyph identities and positions for a specified text string, but does not create cached glyph bitmaps.
old-location: display\strobj_benumpositionsonly.htm
old-project: display
ms.assetid: d5ffe766-843d-4e42-8cc8-bc405e78a2fd
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: STROBJ_bEnumPositionsOnly, STROBJ_bEnumPositionsOnly function [Display Devices], display.strobj_benumpositionsonly, gdifncs_acadb73a-d6b2-4af7-9727-3e5424d30549.xml, winddi/STROBJ_bEnumPositionsOnly
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - STROBJ_bEnumPositionsOnly
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# STROBJ_bEnumPositionsOnly function


## -description


The <b>STROBJ_bEnumPositionsOnly</b> function enumerates glyph identities and positions for a specified text string, but does not create cached glyph bitmaps.


## -parameters




### -param pstro

A caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a> structure describing a text string. This is typically the STROBJ structure received by the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a> function.


### -param pc

A caller-supplied address to receive the GDI-supplied number of GLYPHPOS structures pointed to by the pointer in <i>ppgpos</i>.


### -param ppgpos

A caller-supplied address that receives a GDI-supplied pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff566824">GLYPHPOS</a> structures. (See the following <b>Remarks</b> section.)


## -returns



The return value is <b>TRUE</b> if more glyphs remain to be enumerated, or <b>FALSE</b> if the enumeration is complete. The return value is DDI_ERROR if the glyphs cannot be enumerated, and an error code is logged.




## -remarks



The <b>STROBJ_bEnumPositionsOnly</b> function is typically called from within a driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a> function. It performs the same operations as <a href="https://msdn.microsoft.com/library/windows/hardware/ff569739">STROBJ_bEnum</a> with one important exception − GDI does not create cached bitmaps of the glyphs. The <b>STROBJ_bEnum</b> function assumes the driver will eventually need these bitmaps. However, many newer printers contain internal rasterizers and therefore do not need GDI to render glyphs. For such printers, eliminating the automatic rendering and caching of glyph bitmaps in server memory provides considerable savings of both processing time and memory allocation.

For printers that support internal glyph rasterization, the following rules should be followed:

<ul>
<li>
The driver should set the GCAPS_FONT_RASTERIZER flag in its <a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a> structure.

</li>
<li>
The driver's <i>DrvTextOut</i> function should call <b>STROBJ_bEnumPositionsOnly</b> instead of <b>STROBJ_bEnum</b>.

</li>
<li>
If the print job includes a font that the device cannot rasterize internally, the driver should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff565982">FONTOBJ_cGetGlyphs</a> to obtain glyph bitmaps.

</li>
<li>
If a driver needs to determine the likely printer position after a text string has been printed, but does not need a font glyph, it can call <a href="https://msdn.microsoft.com/library/windows/hardware/ff569741">STROBJ_bGetAdvanceWidths</a>.

</li>
</ul>
Because GDI does not create cached bitmaps of the glyphs, the contents of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566822">GLYPHDEF</a> union within each returned <a href="https://msdn.microsoft.com/library/windows/hardware/ff566824">GLYPHPOS</a> structure will be <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565982">FONTOBJ_cGetGlyphs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566822">GLYPHDEF</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566824">GLYPHPOS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569739">STROBJ_bEnum</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569741">STROBJ_bGetAdvanceWidths</a>
 

 

