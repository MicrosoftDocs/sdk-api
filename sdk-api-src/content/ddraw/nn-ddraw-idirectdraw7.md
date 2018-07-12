---
UID: NN:ddraw.IDirectDraw7
title: IDirectDraw7
author: windows-sdk-content
description: Applications use the methods of the IDirectDraw7 interface to create DirectDraw objects and work with system-level variables. This section is a reference to the methods of the IDirectDraw7 interface.
old-location: directdraw\idirectdraw7.htm
old-project: directdraw
ms.assetid: 1a1164fe-00c2-4469-8346-f86f7f48781e
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: IDirectDraw7, IDirectDraw7 interface [DirectDraw], IDirectDraw7 interface [DirectDraw],described, ddraw/IDirectDraw7, directdraw.idirectdraw7
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ddraw.h
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
tech.root: 
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDraw7 interface


## -description


Applications use the methods of the <b>IDirectDraw7</b> interface to create DirectDraw objects and work with system-level variables. This section is a reference to the methods of the <b>IDirectDraw7</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDraw7</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectDraw7</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDraw7</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn949267">Compact</a>
</td>
<td align="left" width="63%">
This method is not currently implemented.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/123a07c0-d371-4d10-bff8-b5640bd3b920">CreateClipper</a>
</td>
<td align="left" width="63%">
Creates a DirectDrawClipper object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e9eec72-b9c7-4c9f-b9ea-177605fedf96">CreatePalette</a>
</td>
<td align="left" width="63%">
Creates a DirectDrawPalette object for this DirectDraw object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh998978">CreateSurface</a>
</td>
<td align="left" width="63%">
Creates a DirectDrawSurface object for this DirectDraw object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/515219e9-95e9-41fd-9797-d143cd542ef6">DuplicateSurface</a>
</td>
<td align="left" width="63%">
Duplicates a DirectDrawSurface object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04ed2545-c611-435d-95ef-a0d854380a69">EnumDisplayModes</a>
</td>
<td align="left" width="63%">
Enumerates all the display modes that the hardware exposes through the DirectDraw object and that are compatible with a provided surface description.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d97135f3-9921-4e0c-b5ba-e4f709a5e32d">EnumSurfaces</a>
</td>
<td align="left" width="63%">
Enumerates all the existing or possible surfaces that meet the specified surface description.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8027183-07b5-4b7f-8c36-7bd711dac7dd">EvaluateMode</a>
</td>
<td align="left" width="63%">
Used after a call to <a href="https://msdn.microsoft.com/b669e3c7-b34b-4919-9a3e-0349288360ba">IDirectDraw7::StartModeTest</a> to pass or fail each mode that the test presents and to step through the modes until the test is complete.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/495cace2-a315-4937-b0d9-9f77f5d95f66">FlipToGDISurface</a>
</td>
<td align="left" width="63%">
Makes the surface that the GDI writes to the primary surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7bfa81c-8e21-44ec-bed4-9b92aa099f00">GetAvailableVidMem</a>
</td>
<td align="left" width="63%">
Retrieves the total amount of display memory available and the amount of display memory currently free for a given type of surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e93612c-9e28-4d51-a640-e8e9b5ed8e7a">GetCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the device driver for the hardware and the hardware emulation layer (HEL).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1524dae8-e383-47f4-8e18-c8ef235b3176">GetDeviceIdentifier</a>
</td>
<td align="left" width="63%">
Obtains information about the device driver. This method can be used, with caution, to recognize specific hardware installations to implement workarounds for poor driver or chipset behavior.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd31efc8-17c4-4744-a03b-a22a50c7d9c2">GetDisplayMode</a>
</td>
<td align="left" width="63%">
Retrieves the current display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/980b1cfe-d466-42f4-865f-6ddc7a41ea94">GetFourCCCodes</a>
</td>
<td align="left" width="63%">
Retrieves the four-character codes (FOURCC) that are supported by the DirectDraw object. This method can also retrieve the number of codes that are supported.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d0b827d-86f8-4d71-a193-9e330db0fbfd">GetGDISurface</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDrawSurface object that currently represents the surface memory that GDI is treating as the primary surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13f8e5c2-b957-43ce-9fc8-5554c2321bdd">GetMonitorFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the frequency of the monitor that the DirectDraw object controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bccb384-2de3-49a5-962a-31ad2a751e28">GetScanLine</a>
</td>
<td align="left" width="63%">
Retrieves the scan line that is currently being drawn on the monitor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1d96045-a19b-46b0-8b71-5d0bea6889c3">GetSurfaceFromDC</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface for a surface, based on its GDI device context handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bab0d24-ab11-46fb-92de-060f6afe1fde">GetVerticalBlankStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the vertical blank.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a DirectDraw object that was created by using the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> COM function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72897004-cd44-4ca4-bc28-a49bffc09c76">RestoreAllSurfaces</a>
</td>
<td align="left" width="63%">
 Restores all the surfaces that were created for the DirectDraw object, in the order that they were created.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7538339a-8886-4b40-9779-17c8ebe81446">RestoreDisplayMode</a>
</td>
<td align="left" width="63%">
Resets the mode of the display device hardware for the primary surface to what it was before the <a href="https://msdn.microsoft.com/385918cd-64f1-449c-822a-0034a8184fb9">IDirectDraw7::SetDisplayMode</a> method was called. Exclusive-level access is required to use this method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f791732d-9dab-470a-9243-6f71fd3bcd54">SetCooperativeLevel</a>
</td>
<td align="left" width="63%">
Determines the top-level behavior of the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/385918cd-64f1-449c-822a-0034a8184fb9">SetDisplayMode</a>
</td>
<td align="left" width="63%">
Sets the mode of the display-device hardware.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b669e3c7-b34b-4919-9a3e-0349288360ba">StartModeTest</a>
</td>
<td align="left" width="63%">
Initiates a test to update the system registry with refresh rate information for the current display adapter and monitor combination. A call to this method is typically followed by calls to <a href="https://msdn.microsoft.com/c8027183-07b5-4b7f-8c36-7bd711dac7dd">IDirectDraw7::EvaluateMode</a> to pass or fail modes displayed by the test.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bbabd8c-f48e-480c-9ea4-06e4fce1255a">TestCooperativeLevel</a>
</td>
<td align="left" width="63%">
Reports the current cooperative-level status of the DirectDraw device for a windowed or full-screen application.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea52805d-201d-4fbe-a99f-5c04b7d620b5">WaitForVerticalBlank</a>
</td>
<td align="left" width="63%">
Helps the application synchronize itself with the vertical-blank interval.

</td>
</tr>
</table> 


## -remarks



The methods of the <b>IDirectDraw7</b> interface can be organized into the following groups:<table>
<tr>
<th>Group</th>
<th>Methods</th>
</tr>
<tr>
<td>Allocating memory</td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn949267">Compact</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
</tr>
<tr>
<td>Cooperative levels</td>
<td>
<a href="https://msdn.microsoft.com/f791732d-9dab-470a-9243-6f71fd3bcd54">SetCooperativeLevel</a> and <a href="https://msdn.microsoft.com/6bbabd8c-f48e-480c-9ea4-06e4fce1255a">TestCooperativeLevel</a>
</td>
</tr>
<tr>
<td>Creating objects</td>
<td>
<a href="https://msdn.microsoft.com/123a07c0-d371-4d10-bff8-b5640bd3b920">CreateClipper</a>, <a href="https://msdn.microsoft.com/3e9eec72-b9c7-4c9f-b9ea-177605fedf96">CreatePalette</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/hh998978">CreateSurface</a>
</td>
</tr>
<tr>
<td>Device capabilities</td>
<td>
<a href="https://msdn.microsoft.com/4e93612c-9e28-4d51-a640-e8e9b5ed8e7a">GetCaps</a>
</td>
</tr>
<tr>
<td>Display modes</td>
<td>
<a href="https://msdn.microsoft.com/04ed2545-c611-435d-95ef-a0d854380a69">EnumDisplayModes</a>, <a href="https://msdn.microsoft.com/bd31efc8-17c4-4744-a03b-a22a50c7d9c2">GetDisplayMode</a>,  
<a href="https://msdn.microsoft.com/13f8e5c2-b957-43ce-9fc8-5554c2321bdd">GetMonitorFrequency</a>,  
<a href="https://msdn.microsoft.com/7538339a-8886-4b40-9779-17c8ebe81446">RestoreDisplayMode</a>, <a href="https://msdn.microsoft.com/385918cd-64f1-449c-822a-0034a8184fb9">SetDisplayMode</a>,  
and <a href="https://msdn.microsoft.com/ea52805d-201d-4fbe-a99f-5c04b7d620b5">WaitForVerticalBlank</a>
</td>
</tr>
<tr>
<td>Display status</td>
<td>
<a href="https://msdn.microsoft.com/0bccb384-2de3-49a5-962a-31ad2a751e28">GetScanLine</a> and  
  <a href="https://msdn.microsoft.com/4bab0d24-ab11-46fb-92de-060f6afe1fde">GetVerticalBlankStatus</a>
</td>
</tr>
<tr>
<td>Miscellaneous</td>
<td>
<a href="https://msdn.microsoft.com/c8027183-07b5-4b7f-8c36-7bd711dac7dd">EvaluateMode</a>, 
  <a href="https://msdn.microsoft.com/f7bfa81c-8e21-44ec-bed4-9b92aa099f00">GetAvailableVidMem</a>,  
<a href="https://msdn.microsoft.com/1524dae8-e383-47f4-8e18-c8ef235b3176">GetDeviceIdentifier</a>, 
<a href="https://msdn.microsoft.com/980b1cfe-d466-42f4-865f-6ddc7a41ea94">GetFourCCCodes</a>, and  
<a href="https://msdn.microsoft.com/b669e3c7-b34b-4919-9a3e-0349288360ba">StartModeTest</a>
</td>
</tr>
<tr>
<td>Surface management</td>
<td>
<a href="https://msdn.microsoft.com/515219e9-95e9-41fd-9797-d143cd542ef6">DuplicateSurface</a>,  
  <a href="https://msdn.microsoft.com/d97135f3-9921-4e0c-b5ba-e4f709a5e32d">EnumSurfaces</a>,  
<a href="https://msdn.microsoft.com/495cace2-a315-4937-b0d9-9f77f5d95f66">FlipToGDISurface</a>,  
<a href="https://msdn.microsoft.com/4d0b827d-86f8-4d71-a193-9e330db0fbfd">GetGDISurface</a>,  
<a href="https://msdn.microsoft.com/d1d96045-a19b-46b0-8b71-5d0bea6889c3">GetSurfaceFromDC</a>, and 
<a href="https://msdn.microsoft.com/72897004-cd44-4ca4-bc28-a49bffc09c76">RestoreAllSurfaces</a>
</td>
</tr>
</table>
 



The <b>IDirectDraw7</b> interface extends the features of previous versions of the interface by offering methods that enable more flexible surface management than previous versions. All the surface-related methods in the <b>IDirectDraw7</b> interface accept slightly different parameters than their counterparts in the <b>IDirectDraw2</b> interface. Wherever an <b>IDirectDraw2</b> interface method might accept a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550339">DDSURFACEDESC</a> structure and retrieve an <b>IDirectDrawSurface3</b> interface, the methods in <b>IDirectDraw7</b> accept a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550340">DDSURFACEDESC2</a> structure and retrieve an <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface, instead.

<b>IDirectDraw7</b> introduces improved compliance with COM rules that dictate the lifetime of child objects.

Use the LPDIRECTDRAW, LPDIRECTDRAW2, LPDIRECTDRAW4 or LPDIRECTDRAW7 data types to declare a variable that contains a pointer to an <b>IDirectDraw</b>, <b>IDirectDraw2</b>, <b>IDirectDraw4</b> or <b>IDirectDraw7</b> interface. The Ddraw.h header file declares these data types with the following code:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirectDraw     FAR *LPDIRECTDRAW;
typedef struct IDirectDraw2    FAR *LPDIRECTDRAW2;
typedef struct IDirectDraw4    FAR *LPDIRECTDRAW4;
typedef struct IDirectDraw7    FAR *LPDIRECTDRAW7;
</pre>
</td>
</tr>
</table></span></div>


