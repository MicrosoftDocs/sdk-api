---
UID: NF:winddi.DrvTextOut
title: DrvTextOut function
author: windows-sdk-content
description: The DrvTextOut function is the entry point from GDI that calls for the driver to render a set of glyphs at specified positions.
old-location: display\drvtextout.htm
old-project: display
ms.assetid: f2f61687-d833-4d09-8cd5-99e81436c1c1
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: DrvTextOut, DrvTextOut function [Display Devices], ddifncs_e78c3647-65af-427c-8153-0046e031e345.xml, display.drvtextout, winddi/DrvTextOut
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
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
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvTextOut
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvTextOut function


## -description


The <b>DrvTextOut</b> function is the entry point from GDI that calls for the driver to render a set of glyphs at specified positions.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that describes the surface on which to write.


### -param pstro

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a> structure that defines the glyphs to be rendered and the positions in which to place them.


### -param pfo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure from which to retrieve information about the font and its glyphs.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure that defines the clip region through which all rendering must be done. The driver cannot affect any pixels outside the clip region.


### -param prclExtra

Pointer to a RECTL structure. GDI always sets this parameter to <b>NULL</b> in calls to this function. It should be ignored by the driver.


### -param prclOpaque

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that represents a single opaque rectangle. This rectangle is lower-right exclusive. Pixels within this rectangle (those that are not foreground and not clipped) are to be rendered with the opaque brush. This rectangle always bounds the text to be drawn. If this parameter is <b>NULL</b>, no opaque pixels are to be rendered.


### -param pboFore

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a> structure that represents the brush object to be used for the foreground pixels. This brush will always be a solid color brush.


### -param pboOpaque

Pointer to a BRUSHOBJ structure that represents the opaque pixels. Both the foreground and background mix modes for this brush are assumed to be R2_COPYPEN. Unless the driver sets the GCAPS_ARBRUSHOPAQUE capabilities bit in the <b>flGraphicsCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a> structure, it will always be called with a solid color brush.


### -param pptlOrg

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that defines the brush origin for both brushes.


### -param mix

The mix mode that defines the foreground and background raster operations to use for the brush that <i>pboFore</i> points to. For more information about mix mode, see Remarks. 


## -returns



The return value is <b>TRUE</b> if the function is successful; otherwise, it is <b>FALSE</b>.




## -remarks



The input parameters to <b>DrvTextOut</b> define two sets of pixels: foreground and opaque. The driver must render the surface so that the result is identical to a process where the opaque pixels are rendered first with the opaque brush, and then the foreground pixels are rendered with the foreground brush. Each of these operations is limited by clipping.

The foreground and opaque pixels are regarded as a screen through which color is brushed onto the surface. The glyphs of the font do not have color in themselves.

The input parameters to <b>DrvTextOut</b> define the set of glyph pixels, the set of extra rectangles, the opaque rectangle, and the clip region. It is the driver's responsibility to calculate and then render the set of foreground and opaque pixels.

GDI guarantees that <b>DrvTextOut</b> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff556192">DrvDestroyFont</a> never overlap; consequently, the driver can rely on cached information while processing a <b>DrvTextOut</b> call.

The mix mode defines how the incoming pattern should be mixed with the data that is already on the device surface. The MIX data type consists of two binary raster operation (ROP2) values packed into a single ULONG. The lowest-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.

This is a conditionally required function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556192">DrvDestroyFont</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

