---
UID: NS:ddrawint._DD_BLTDATA
title: "_DD_BLTDATA"
author: windows-sdk-content
description: The DD_BLTDATA structure contains the information relevant to the driver for doing bit block transfers.
old-location: display\dd_bltdata.htm
old-project: display
ms.assetid: e39bdfc4-89d0-4440-93d3-1b455cc9a8e5
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PDD_BLTDATA, DD_BLTDATA, DD_BLTDATA structure [Display Devices], _DD_BLTDATA, ddrawint/DD_BLTDATA, ddstrcts_0697bd98-66f4-4f58-b407-c3bcc73eee86.xml, display.dd_bltdata"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
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
tech.root: 
req.typenames: "*PDD_BLTDATA, DD_BLTDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddrawint.h
api_name:
-	DD_BLTDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_BLTDATA structure


## -description


The DD_BLTDATA structure contains the information relevant to the driver for doing bit block transfers.  


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550586">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field lpDDDestSurface

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure that describes the surface on which to blit.


### -field rDest



###### 



###### 



###### 


### -field lpDDSrcSurface

Points to a DD_SURFACE_LOCAL structure that describes the source surface.


### -field rSrc



###### 



###### 



###### 


### -field dwFlags

Indicates a set of flags that specify the type of blit operation to perform and what associated structure members have valid data that the driver should use. This member is a bitwise OR of any of the following flags:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDBLT_ASYNC

</td>
<td>
Perform this blit asynchronously through the FIFO in the order received. If no room exists in the hardware FIFO, the driver should fail the call and return immediately.

</td>
</tr>
<tr>
<td>
DDBLT_COLORFILL

</td>
<td>
Use the <b>dwFillColor</b> member in the DDBLTFX structure (defined in the Microsoft DirectDraw SDK documentation) as the RGB color with which to fill the destination rectangle on the destination surface.

</td>
</tr>
<tr>
<td>
DDBLT_DDFX

</td>
<td>
Use the <b>dwDDFX</b> member in the DDBLTFX structure (defined in the DirectDraw SDK documentation) to determine the effects to use for the blit.

</td>
</tr>
<tr>
<td>
DDBLT_DDROPS

</td>
<td>
This flag is reserved for system use and should be ignored by the driver. The driver should also ignore the <b>dwDDROPS</b> member of the DDBLTFX structure.

</td>
</tr>
<tr>
<td>
DDBLT_EXTENDED_FLAGS

</td>
<td>

<dl>
<dt><b>Microsoft DirectX 9.0 and later versions only.</b></dt>
<dt>Set by the runtime to direct the driver to reinterpret certain flags in <b>dwFlags</b> from their meanings in DirectX 8.1 and earlier versions. The runtime combines DDBLT_EXTENDED_FLAGS with DDBLT_<i>Xxx</i> flags using a bitwise OR to create DDBLT_EXTENDED_<i>Xxx</i> flags.</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDBLT_EXTENDED_LINEAR_CONTENT

</td>
<td>

<dl>
<dt><b>Microsoft DirectX 9.0 and later versions only.</b></dt>
<dt>Created through the bitwise OR combination of DDBLT_EXTENDED_FLAGS and the 0x00000004 bit.</dt>
<dt>Indicates that the source surface contains content in a linear color space. The driver can then perform gamma 2.2 correction (sRGB) to the desktop color space as part of the blt.</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDBLT_EXTENDED_PRESENTATION_STRETCHFACTOR

</td>
<td>

<dl>
<dt><b>Microsoft DirectX 9.0 and later versions only.</b></dt>
<dt><b>NT-based operating systems only.</b></dt>
<dt>Created through the bitwise OR combination of DDBLT_EXTENDED_FLAGS and the 0x00000010 bit. </dt>
<dt>Set if the runtime subsequently uses the DDBLT_PRESENTATION and DDBLT_LAST_PRESENTATION flags to request a series of stretch-blit operations because of a <b>Present</b> call by an application.</dt>
<dt>Notifies the driver about the entire unclipped source and destination rectangular areas before the driver receives actual sub-rectangular areas for blits. In this way, the driver can calculate and record the stretch factor for all subsequent blits up to and including the blit with the DDBLT_LAST_PRESENTATION flag set. However, when the driver receives a blit with the DDBLT_EXTENDED_PRESENTATION_STRETCHFACTOR flag set, the driver must not use these unclipped rectangular areas to do any actual blitting.</dt>
<dt>After the driver finishes the final blit with the DDBLT_LAST_PRESENTATION flag set, the driver should clear the stretch-factor record to prevent interference with any subsequent blits</dt>
</dl> .

</td>
</tr>
<tr>
<td>
DDBLT_KEYDESTOVERRIDE

</td>
<td>
Use the <b>dckDestColorkey</b> member in the DDBLTFX structure (defined in the DirectDraw SDK documentation) as the color key for the destination surface. If an override is not being set, then <b>dckDestColorkey</b> does not contain the color key. The driver should test the surface itself.

</td>
</tr>
<tr>
<td>
DDBLT_KEYSRCOVERRIDE

</td>
<td>
Use the <b>dckSrcColorkey</b> member in the DDBLTFX structure (defined in the DirectDraw SDK documentation) as the color key for the source surface. If an override is not being set, then <b>dckDestColorkey</b> does not contain the color key. The driver should test the surface itself.

</td>
</tr>
<tr>
<td>
DDBLT_LAST_PRESENTATION

</td>
<td>

<dl>
<dt><b>DirectX 8.0 and later versions only.</b></dt>
<dt>Set if the runtime requests a final blit operation because of a <b>Present</b> call by an application.</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDBLT_PRESENTATION

</td>
<td>

<dl>
<dt><b>DirectX 8.0 and later versions only.</b></dt>
<dt>Set if the runtime requests a blit operation because of a <b>Present</b> call by an application.</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDBLT_ROP

</td>
<td>
Use the <b>dwROP</b> member in the DDBLTFX structure (defined in the DirectDraw SDK documentation) for the raster operation for this blit. Currently, the only <a href="https://msdn.microsoft.com/004698f5-cb0e-4995-a19c-7075aa226000">ROP</a> passed to the driver is SRCCOPY. This ROP is the same as that defined in the Win32 API. See the Microsoft Windows SDK documentation for details.

</td>
</tr>
<tr>
<td>
DDBLT_ROTATIONANGLE

</td>
<td>
This flag is not supported on Windows 2000 and later and should be ignored by the driver.

</td>
</tr>
<tr>
<td>
DDBLT_WAIT

</td>
<td>
Do not return immediately with the DDERR_WASSTILLDRAWING message if the blitter is busy--wait until the blit can be set up or another error occurs.

</td>
</tr>
</table>
 


### -field dwROPFlags

Unused on Windows 2000 and later and should be ignored by the driver.


### -field bltFX



######### 



###### 



####### 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/28e0c827-33f1-4b83-9f20-bbb66bc0e14a">DdBlt</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field Blt

Used by the DirectDraw API and should not be filled in by the driver.


### -field IsClipped

Indicates whether this is a clipped blit. On Windows 2000 and later, this member is always <b>FALSE</b>, indicating that the blit is unclipped.


### -field rOrigDest

<b>Unused for Windows 2000 and later.</b> Specifies a RECTL structure that defines the unclipped destination rectangle. This member is valid only if <b>IsClipped</b> is <b>TRUE</b>. 


### -field rOrigSrc

<b>Unused for Windows 2000 and later.</b> Specifies a RECTL structure that defines the unclipped source rectangle. This member is valid only if <b>IsClipped</b> is <b>TRUE</b>.


### -field dwRectCnt

<b>Unused for Windows 2000 and later.</b>
       Specifies the number of destination rectangles to which <b>prDestRects</b> points. This member is valid only if <b>IsClipped</b> is <b>TRUE</b>.


### -field prDestRects

<b>Unused for Windows 2000 and later.</b> Points to an array of RECTL structures that describe of destination rectangles. This member is valid only if <b>IsClipped</b> is <b>TRUE</b>.


### -field dwAFlags

Unused and should be ignored by the driver.


### -field ddargbScaleFactors

ARGB scaling factors (AlphaBlt)


## -remarks



For more information about the DDBLT_PRESENTATION and DDBLT_LAST_PRESENTATION flags, see <a href="https://msdn.microsoft.com/23a01b5b-0654-4c43-ac96-a75810fa20df">Presentation</a>. 




## -see-also




<a href="https://msdn.microsoft.com/28e0c827-33f1-4b83-9f20-bbb66bc0e14a">DdBlt</a>
 

 

