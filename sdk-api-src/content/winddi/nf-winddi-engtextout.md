---
UID: NF:winddi.EngTextOut
title: EngTextOut function
author: windows-sdk-content
description: The EngTextOut function causes GDI to render a set of glyphs at specified positions.
old-location: display\engtextout.htm
old-project: display
ms.assetid: 7891692e-a4e1-401a-99e0-ed8135dc6f1d
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EngTextOut, EngTextOut function [Display Devices], display.engtextout, gdifncs_e383ce94-952d-48e3-a814-afd38822aad2.xml, winddi/EngTextOut
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
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
 - EngTextOut
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngTextOut function


## -description


The <b>EngTextOut</b> function causes GDI to render a set of glyphs at specified positions.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that describes the surface on which to write.


### -param pstro

Pointer to a <a href="https://msdn.microsoft.com/efe53cb8-39b9-4931-bac2-9c61efd9d457">STROBJ</a> structure that defines the glyphs to be rendered and the positions where they are to be placed.


### -param pfo

Pointer to a <a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a> structure that is used to retrieve information about the font and its glyphs.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure that defines the clip region through which rendering must be done. No pixels can be affected outside this clip region.


### -param prclExtra

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure. This parameter should always be <b>NULL</b>.


### -param prclOpaque

Pointer to a RECTL structure that identifies a single opaque rectangle that is lower-right exclusive. Pixels within this rectangle (those that are not foreground and not clipped) are to be rendered with the opaque brush. This rectangle always bounds the text to be drawn. If this parameter is <b>NULL</b>, no opaque pixels are to be rendered.


### -param pboFore

Pointer to a <a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a> structure that represents the brush object to be used for the foreground pixels. This brush will always be a solid color brush.


### -param pboOpaque

Pointer to a BRUSHOBJ structure that represents the brush object for the opaque pixels. Both the foreground and background mix modes for this brush are assumed to be R2_COPYPEN. Unless the driver sets the GCAPS_ARBRUSHOPAQUE capabilities bit in the <b>flGraphicsCaps</b> member of the <a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a> structure, it will always be called with a solid color brush.


### -param pptlOrg

Pointer to a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that defines the brush origin for both brushes. If this parameter is set to 0 when <b>EngTextOut</b> is called, some printer drivers may print color images incorrectly. For more information, see <b>Remarks</b>.


### -param mix [in]

Specifies foreground and background raster operations (mix modes) for <i>pboFore</i>.


## -returns



The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.




## -remarks



The driver should call <b>EngTextOut</b> when it has hooked <a href="https://msdn.microsoft.com/f2f61687-d833-4d09-8cd5-99e81436c1c1">DrvTextOut</a> and cannot render the glyphs.

<div class="alert"><b>Note</b>    The driver cannot punt to <b>EngTextOut</b> if it has hooked <i>DrvTextOut</i> for a device managed surface.</div>
<div> </div>
The input parameters to <b>EngTextOut</b> define two sets of pixels: foreground and opaque. The driver must render the surface so the result is identical to a process where the opaque pixels are rendered first with the opaque brush, and then the foreground pixels are rendered with the foreground brush. Each of these operations is limited by clipping.

When the <i>pptlOrg</i> parameter of this function is set to 0, some printer drivers print color images incorrectly in Microsoft Windows Server 2003 (Japanese version). Setting <i>pptlOrg</i> to 0, a <b>NULL</b> pointer value, is interpreted to mean that no brush origin is defined. To prevent this problem, initialize <i>pptlOrg</i> with the address of a POINTL structure whose members are set to (0,0), prior to the call to <b>EngTextOut</b>.

The foreground and opaque pixels are regarded as a screen through which color is brushed onto the surface. The glyphs of the font do not have color in themselves.

The input parameters to <b>EngTextOut</b> define the set of glyph pixels, the set of extra rectangles, the opaque rectangle, and the clip region. The driver must calculate and then render the set of foreground and opaque pixels.

The mix mode defines how the incoming pattern should be mixed with the data already on the device surface. The MIX data type consists of two ROP2 values packed into a single ULONG. The low-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a>



<a href="https://msdn.microsoft.com/f2f61687-d833-4d09-8cd5-99e81436c1c1">DrvTextOut</a>



<a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a>



<a href="https://msdn.microsoft.com/efe53cb8-39b9-4931-bac2-9c61efd9d457">STROBJ</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 

