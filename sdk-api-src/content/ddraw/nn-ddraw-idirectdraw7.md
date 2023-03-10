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

The <b>IDirectDraw7</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDraw7</b> also has these types of members:

## -remarks

The methods of the <b>IDirectDraw7</b> interface can be organized into the following groups:<table>
<tr>
<th>Group</th>
<th>Methods</th>
</tr>
<tr>
<td>Allocating memory</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-compact">Compact</a> and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-initialize">Initialize</a>
</td>
</tr>
<tr>
<td>Cooperative levels</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-setcooperativelevel">SetCooperativeLevel</a> and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-testcooperativelevel">TestCooperativeLevel</a>
</td>
</tr>
<tr>
<td>Creating objects</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createclipper">CreateClipper</a>, <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createpalette">CreatePalette</a>, and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createsurface">CreateSurface</a>
</td>
</tr>
<tr>
<td>Device capabilities</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getcaps">GetCaps</a>
</td>
</tr>
<tr>
<td>Display modes</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-enumdisplaymodes">EnumDisplayModes</a>, <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getdisplaymode">GetDisplayMode</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getmonitorfrequency">GetMonitorFrequency</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-restoredisplaymode">RestoreDisplayMode</a>, <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-setdisplaymode">SetDisplayMode</a>,  
and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-waitforverticalblank">WaitForVerticalBlank</a>
</td>
</tr>
<tr>
<td>Display status</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getscanline">GetScanLine</a> and  
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getverticalblankstatus">GetVerticalBlankStatus</a>
</td>
</tr>
<tr>
<td>Miscellaneous</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-evaluatemode">EvaluateMode</a>, 
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getavailablevidmem">GetAvailableVidMem</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getdeviceidentifier">GetDeviceIdentifier</a>, 
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getfourcccodes">GetFourCCCodes</a>, and  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-startmodetest">StartModeTest</a>
</td>
</tr>
<tr>
<td>Surface management</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-duplicatesurface">DuplicateSurface</a>,  
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-enumsurfaces">EnumSurfaces</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-fliptogdisurface">FlipToGDISurface</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getgdisurface">GetGDISurface</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getsurfacefromdc">GetSurfaceFromDC</a>, and 
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-restoreallsurfaces">RestoreAllSurfaces</a>
</td>
</tr>
</table>
 



The <b>IDirectDraw7</b> interface extends the features of previous versions of the interface by offering methods that enable more flexible surface management than previous versions. All the surface-related methods in the <b>IDirectDraw7</b> interface accept slightly different parameters than their counterparts in the <b>IDirectDraw2</b> interface. Wherever an <b>IDirectDraw2</b> interface method might accept a <a href="/windows/win32/api/ddraw/ns-ddraw-ddsurfacedesc">DDSURFACEDESC</a> structure and retrieve an <b>IDirectDrawSurface3</b> interface, the methods in <b>IDirectDraw7</b> accept a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure and retrieve an <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface, instead.

<b>IDirectDraw7</b> introduces improved compliance with COM rules that dictate the lifetime of child objects.

Use the LPDIRECTDRAW, LPDIRECTDRAW2, LPDIRECTDRAW4 or LPDIRECTDRAW7 data types to declare a variable that contains a pointer to an <b>IDirectDraw</b>, <b>IDirectDraw2</b>, <b>IDirectDraw4</b> or <b>IDirectDraw7</b> interface. The Ddraw.h header file declares these data types with the following code:


```

typedef struct IDirectDraw     FAR *LPDIRECTDRAW;
typedef struct IDirectDraw2    FAR *LPDIRECTDRAW2;
typedef struct IDirectDraw4    FAR *LPDIRECTDRAW4;
typedef struct IDirectDraw7    FAR *LPDIRECTDRAW7;

```
