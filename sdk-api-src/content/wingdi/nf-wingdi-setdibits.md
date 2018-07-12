---
UID: NF:wingdi.SetDIBits
title: SetDIBits function
author: windows-sdk-content
description: The SetDIBits function sets the pixels in a compatible bitmap (DDB) using the color data found in the specified DIB.
old-location: gdi\setdibits.htm
old-project: gdi
ms.assetid: 706f4532-4073-4d5c-ae2d-e33aea9163e9
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: DIB_PAL_COLORS, DIB_RGB_COLORS, SetDIBits, SetDIBits function [Windows GDI], _win32_SetDIBits, gdi.setdibits, wingdi/SetDIBits
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetDIBits
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetDIBits function


## -description


The <b>SetDIBits</b> function sets the pixels in a compatible bitmap (DDB) using the color data found in the specified DIB.


## -parameters




### -param hdc [in]

A handle to a device context.


### -param hbm

TBD


### -param start

TBD


### -param cLines

TBD


### -param lpBits

TBD


### -param lpbmi [in]

A pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure that contains information about the DIB.


### -param ColorUse

TBD




#### - cScanLines [in]

The number of scan lines found in the array containing device-independent color data.


#### - fuColorUse [in]

Indicates whether the <b>bmiColors</b> member of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure was provided and, if so, whether <b>bmiColors</b> contains explicit red, green, blue (RGB) values or palette indexes. The <i>fuColorUse</i> parameter must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DIB_PAL_COLORS"></a><a id="dib_pal_colors"></a><dl>
<dt><b>DIB_PAL_COLORS</b></dt>
</dl>
</td>
<td width="60%">
The color table consists of an array of 16-bit indexes into the logical palette of the device context identified by the <i>hdc</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="DIB_RGB_COLORS"></a><a id="dib_rgb_colors"></a><dl>
<dt><b>DIB_RGB_COLORS</b></dt>
</dl>
</td>
<td width="60%">
The color table is provided and contains literal RGB values.

</td>
</tr>
</table>
 


#### - hbmp [in]

A handle to the compatible bitmap (DDB) that is to be altered using the color data from the specified DIB.


#### - lpvBits [in]

A pointer to the DIB color data, stored as an array of bytes. The format of the bitmap values depends on the <b>biBitCount</b> member of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure pointed to by the <i>lpbmi</i> parameter.


#### - uStartScan [in]

The starting scan line for the device-independent color data in the array pointed to by the <i>lpvBits</i> parameter.


## -returns



If the function succeeds, the return value is the number of scan lines copied.

If the function fails, the return value is zero.

This can be the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters is invalid.

</td>
</tr>
</table>
 




## -remarks



Optimal bitmap drawing speed is obtained when the bitmap bits are indexes into the system palette.

Applications can retrieve the system palette colors and indexes by calling the <a href="https://msdn.microsoft.com/67bb0adf-ae7f-48d5-bc62-82ece45aeee6">GetSystemPaletteEntries</a> function. After the colors and indexes are retrieved, the application can create the DIB. For more information, see <a href="https://msdn.microsoft.com/4c93ce8c-6b3a-4016-bb47-786c25b93374">System Palette</a>.

The device context identified by the <i>hdc</i> parameter is used only if the DIB_PAL_COLORS constant is set for the <i>fuColorUse</i> parameter; otherwise it is ignored.

The bitmap identified by the <i>hbmp</i> parameter must not be selected into a device context when the application calls this function.

The scan lines must be aligned on a <b>DWORD</b> except for RLE-compressed bitmaps.

The origin for bottom-up DIBs is the lower-left corner of the bitmap; the origin for top-down DIBs is the upper-left corner of the bitmap.

<b>ICM:</b> Color management is performed if color management has been enabled with a call to <a href="https://msdn.microsoft.com/40d70c1f-c580-43c4-b44b-6c9388e138fb">SetICMMode</a> with the <i>iEnableICM</i> parameter set to ICM_ON. If the bitmap specified by <i>lpbmi</i> has a <a href="https://msdn.microsoft.com/17c50d55-1c95-4178-82ba-7f504aa63c83">BITMAPV4HEADER</a> that specifies the gamma and endpoints members, or a <a href="https://msdn.microsoft.com/ec5db6f9-93fa-4dbe-afdb-c039292b26e3">BITMAPV5HEADER</a> that specifies either the gamma and endpoints members or the profileData and profileSize members, then the call treats the bitmap's pixels as being expressed in the color space described by those members, rather than in the device context's source color space.




## -see-also




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a>



<a href="https://msdn.microsoft.com/67bb0adf-ae7f-48d5-bc62-82ece45aeee6">GetSystemPaletteEntries</a>
 

 

