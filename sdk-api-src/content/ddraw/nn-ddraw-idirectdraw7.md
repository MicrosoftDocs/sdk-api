---
UID: NN:ddraw.IDirectDraw7
title: IDirectDraw7 (ddraw.h)
description: Applications use the methods of the IDirectDraw7 interface to create DirectDraw objects and work with system-level variables. This section is a reference to the methods of the IDirectDraw7 interface.
helpviewer_keywords: ["IDirectDraw7","IDirectDraw7 interface [DirectDraw]","IDirectDraw7 interface [DirectDraw]","described","ddraw/IDirectDraw7","directdraw.idirectdraw7"]
old-location: directdraw\idirectdraw7.htm
tech.root: directdraw
ms.assetid: 1a1164fe-00c2-4469-8346-f86f7f48781e
ms.date: 12/05/2018
ms.keywords: IDirectDraw7, IDirectDraw7 interface [DirectDraw], IDirectDraw7 interface [DirectDraw],described, ddraw/IDirectDraw7, directdraw.idirectdraw7
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDraw7
 - ddraw/IDirectDraw7
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7
---

# IDirectDraw7 interface


## -description

Applications use the methods of the <b>IDirectDraw7</b> interface to create DirectDraw objects and work with system-level variables. This section is a reference to the methods of the <b>IDirectDraw7</b> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDraw7</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDraw7</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-compact">Compact</a>
</td>
<td align="left" width="63%">
This method is not currently implemented.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createclipper">CreateClipper</a>
</td>
<td align="left" width="63%">
Creates a DirectDrawClipper object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createpalette">CreatePalette</a>
</td>
<td align="left" width="63%">
Creates a DirectDrawPalette object for this DirectDraw object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createsurface">CreateSurface</a>
</td>
<td align="left" width="63%">
Creates a DirectDrawSurface object for this DirectDraw object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-duplicatesurface">DuplicateSurface</a>
</td>
<td align="left" width="63%">
Duplicates a DirectDrawSurface object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-enumdisplaymodes">EnumDisplayModes</a>
</td>
<td align="left" width="63%">
Enumerates all the display modes that the hardware exposes through the DirectDraw object and that are compatible with a provided surface description.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-enumsurfaces">EnumSurfaces</a>
</td>
<td align="left" width="63%">
Enumerates all the existing or possible surfaces that meet the specified surface description.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-evaluatemode">EvaluateMode</a>
</td>
<td align="left" width="63%">
Used after a call to <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-startmodetest">IDirectDraw7::StartModeTest</a> to pass or fail each mode that the test presents and to step through the modes until the test is complete.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-fliptogdisurface">FlipToGDISurface</a>
</td>
<td align="left" width="63%">
Makes the surface that the GDI writes to the primary surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getavailablevidmem">GetAvailableVidMem</a>
</td>
<td align="left" width="63%">
Retrieves the total amount of display memory available and the amount of display memory currently free for a given type of surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getcaps">GetCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the device driver for the hardware and the hardware emulation layer (HEL).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getdeviceidentifier">GetDeviceIdentifier</a>
</td>
<td align="left" width="63%">
Obtains information about the device driver. This method can be used, with caution, to recognize specific hardware installations to implement workarounds for poor driver or chipset behavior.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getdisplaymode">GetDisplayMode</a>
</td>
<td align="left" width="63%">
Retrieves the current display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getfourcccodes">GetFourCCCodes</a>
</td>
<td align="left" width="63%">
Retrieves the four-character codes (FOURCC) that are supported by the DirectDraw object. This method can also retrieve the number of codes that are supported.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getgdisurface">GetGDISurface</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDrawSurface object that currently represents the surface memory that GDI is treating as the primary surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getmonitorfrequency">GetMonitorFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the frequency of the monitor that the DirectDraw object controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getscanline">GetScanLine</a>
</td>
<td align="left" width="63%">
Retrieves the scan line that is currently being drawn on the monitor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getsurfacefromdc">GetSurfaceFromDC</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for a surface, based on its GDI device context handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getverticalblankstatus">GetVerticalBlankStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the vertical blank.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a DirectDraw object that was created by using the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> COM function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-restoreallsurfaces">RestoreAllSurfaces</a>
</td>
<td align="left" width="63%">
 Restores all the surfaces that were created for the DirectDraw object, in the order that they were created.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-restoredisplaymode">RestoreDisplayMode</a>
</td>
<td align="left" width="63%">
Resets the mode of the display device hardware for the primary surface to what it was before the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-setdisplaymode">IDirectDraw7::SetDisplayMode</a> method was called. Exclusive-level access is required to use this method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-setcooperativelevel">SetCooperativeLevel</a>
</td>
<td align="left" width="63%">
Determines the top-level behavior of the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-setdisplaymode">SetDisplayMode</a>
</td>
<td align="left" width="63%">
Sets the mode of the display-device hardware.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-startmodetest">StartModeTest</a>
</td>
<td align="left" width="63%">
Initiates a test to update the system registry with refresh rate information for the current display adapter and monitor combination. A call to this method is typically followed by calls to <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-evaluatemode">IDirectDraw7::EvaluateMode</a> to pass or fail modes displayed by the test.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-testcooperativelevel">TestCooperativeLevel</a>
</td>
<td align="left" width="63%">
Reports the current cooperative-level status of the DirectDraw device for a windowed or full-screen application.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-waitforverticalblank">WaitForVerticalBlank</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-compact">Compact</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-initialize">Initialize</a>
</td>
</tr>
<tr>
<td>Cooperative levels</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-setcooperativelevel">SetCooperativeLevel</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-testcooperativelevel">TestCooperativeLevel</a>
</td>
</tr>
<tr>
<td>Creating objects</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createclipper">CreateClipper</a>, <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createpalette">CreatePalette</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createsurface">CreateSurface</a>
</td>
</tr>
<tr>
<td>Device capabilities</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getcaps">GetCaps</a>
</td>
</tr>
<tr>
<td>Display modes</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-enumdisplaymodes">EnumDisplayModes</a>, <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getdisplaymode">GetDisplayMode</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getmonitorfrequency">GetMonitorFrequency</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-restoredisplaymode">RestoreDisplayMode</a>, <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-setdisplaymode">SetDisplayMode</a>,  
and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-waitforverticalblank">WaitForVerticalBlank</a>
</td>
</tr>
<tr>
<td>Display status</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getscanline">GetScanLine</a> and  
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getverticalblankstatus">GetVerticalBlankStatus</a>
</td>
</tr>
<tr>
<td>Miscellaneous</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-evaluatemode">EvaluateMode</a>, 
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getavailablevidmem">GetAvailableVidMem</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getdeviceidentifier">GetDeviceIdentifier</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getfourcccodes">GetFourCCCodes</a>, and  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-startmodetest">StartModeTest</a>
</td>
</tr>
<tr>
<td>Surface management</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-duplicatesurface">DuplicateSurface</a>,  
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-enumsurfaces">EnumSurfaces</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-fliptogdisurface">FlipToGDISurface</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getgdisurface">GetGDISurface</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getsurfacefromdc">GetSurfaceFromDC</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-restoreallsurfaces">RestoreAllSurfaces</a>
</td>
</tr>
</table>
 



The <b>IDirectDraw7</b> interface extends the features of previous versions of the interface by offering methods that enable more flexible surface management than previous versions. All the surface-related methods in the <b>IDirectDraw7</b> interface accept slightly different parameters than their counterparts in the <b>IDirectDraw2</b> interface. Wherever an <b>IDirectDraw2</b> interface method might accept a <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)">DDSURFACEDESC</a> structure and retrieve an <b>IDirectDrawSurface3</b> interface, the methods in <b>IDirectDraw7</b> accept a <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure and retrieve an <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface, instead.

<b>IDirectDraw7</b> introduces improved compliance with COM rules that dictate the lifetime of child objects.

Use the LPDIRECTDRAW, LPDIRECTDRAW2, LPDIRECTDRAW4 or LPDIRECTDRAW7 data types to declare a variable that contains a pointer to an <b>IDirectDraw</b>, <b>IDirectDraw2</b>, <b>IDirectDraw4</b> or <b>IDirectDraw7</b> interface. The Ddraw.h header file declares these data types with the following code:


```

typedef struct IDirectDraw     FAR *LPDIRECTDRAW;
typedef struct IDirectDraw2    FAR *LPDIRECTDRAW2;
typedef struct IDirectDraw4    FAR *LPDIRECTDRAW4;
typedef struct IDirectDraw7    FAR *LPDIRECTDRAW7;

```

