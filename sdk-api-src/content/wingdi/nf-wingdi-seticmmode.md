---
UID: NF:wingdi.SetICMMode
title: SetICMMode function
author: windows-sdk-content
description: The SetICMMode function causes Image Color Management to be enabled, disabled, or queried on a given device context (DC).
old-location: wcs\seticmmode.htm
old-project: WCS
ms.assetid: 40d70c1f-c580-43c4-b44b-6c9388e138fb
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ICM_DONE_OUTSIDEDC, ICM_OFF, ICM_ON, ICM_QUERY, SetICMMode, SetICMMode function [Windows Color System], _color_SetICMMode, wcs.seticmmode, wingdi/SetICMMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: 
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
 - Gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
api_name:
 - SetICMMode
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetICMMode function


## -description


The <b>SetICMMode</b> function causes Image Color Management to be enabled, disabled, or queried on a given device context (DC).


## -parameters




### -param hdc

TBD


### -param mode

TBD




#### - hDC

Identifies handle to the device context.


#### - iEnableICM

Turns on and off image color management. This parameter can take one of the following constant values.<div> </div>


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICM_ON"></a><a id="icm_on"></a><dl>
<dt><b>ICM_ON</b></dt>
</dl>
</td>
<td width="60%">
Turns on color management. Turns off old-style color correction of halftones.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_OFF"></a><a id="icm_off"></a><dl>
<dt><b>ICM_OFF</b></dt>
</dl>
</td>
<td width="60%">
Turns off color management. Turns on old-style color correction of halftones.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_QUERY"></a><a id="icm_query"></a><dl>
<dt><b>ICM_QUERY</b></dt>
</dl>
</td>
<td width="60%">
Queries the current state of color management.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_DONE_OUTSIDEDC"></a><a id="icm_done_outsidedc"></a><dl>
<dt><b>ICM_DONE_OUTSIDEDC</b></dt>
</dl>
</td>
<td width="60%">
Turns off color management inside DC. Under Windows 2000, also turns off old-style color correction of halftones. Not supported under Windows 95.

</td>
</tr>
</table>
 


## -returns



If this function succeeds, the return value is a nonzero value.

If this function fails, the return value is zero.

If ICM_QUERY is specified and the function succeeds, the nonzero value returned is ICM_ON or ICM_OFF to indicate the current mode.




## -remarks



If the system cannot find an ICC color profile to match the state of the device, <b>SetICMMode</b> fails and returns zero.

Once WCS is enabled for a device context (DC), colors passed into the DC using most Win32 API functions are color matched. The primary exceptions are <b>BitBlt</b> and <b>StretchBlt</b>. The assumption is that when performing a bit block transfer (blit) from one DC to another, the two DCs are already compatible and need no color correction. If this is not the case, color correction may be performed. Specifically, if a device independent bitmap (DIB) is used as the source for a blit, and the blit is performed into a DC that has WCS enabled, color matching will be performed. If this is not what you want, turn WCS off for the destination DC by calling <b>SetICMMode</b> before calling <b>BitBlt</b> or <b>StretchBlt</b>.

If the <b>CreateCompatibleDC</b> function is used to create a bitmap in a DC, it is possible for the bitmap to be color matched twice, once when it is created and once when a blit is performed. The reason is that a bitmap in a DC created by the <b>CreateCompatibleDC</b> function acquires the current brush, pens, and palette of the source DC. However, WCS will be disabled by default for the new DC. If WCS is later enabled for the new DC by using the <b>SetICMMode</b> function, a color correction will be done. To prevent double color corrections through the use of the <b>CreateCompatibleDC</b> function, use the <b>SetICMMode</b> function to turn WCS off for the source DC before the <b>CreateCompatibleDC</b> function is called.

When a compatible DC is created from a printer's DC (see <b>CreateCompatibleDC</b> ), the default is for color matching to always be performed if it is enabled for the printer's DC. The default color profile for the printer is used when a blit is performed into the printer's DC using <b>SetDIBitsToDevice</b> or <b>StretchDIBits</b>. If this is not what you want, turn WCS off for the printer's DC by calling <b>SetICMMode</b> before calling <b>SetDIBitsToDevice</b> or <b>StretchDIBits</b>.

Also, when printing to a printer's DC with WCS turned on, the <b>SetICMMode</b> function needs to be called after every call to the <b>StartPage</b> function to turn back on WCS. The <b>StartPage</b> function calls the <b>RestoreDC</b> and <b>SaveDC</b> functions, which result in WCS being turned off for the printer's DC.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/d6a181e4-b6cf-44b7-bf47-4900272d6d72">BitBlt</a>



<a href="https://msdn.microsoft.com/6ddc3705-2995-41af-af94-258aed597e17">CreateCompatibleDC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/41225400-12e3-47ba-8b88-ac1d5b0fa90f">SetDIBitsToDevice</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a>



<a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a>



<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a>
 

 

