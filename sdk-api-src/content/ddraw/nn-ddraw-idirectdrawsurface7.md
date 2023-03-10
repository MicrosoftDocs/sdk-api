---
UID: NN:ddraw.IDirectDrawSurface7
title: IDirectDrawSurface7 (ddraw.h)
description: Applications use the methods of the IDirectDrawSurface7 interface to create DirectDrawSurface objects and work with system-level variables. This section is a reference to the methods of this interface.
helpviewer_keywords: ["IDirectDrawSurface7","IDirectDrawSurface7 interface [DirectDraw]","IDirectDrawSurface7 interface [DirectDraw]","described","ddraw/IDirectDrawSurface7","directdraw.idirectdrawsurface7"]
old-location: directdraw\idirectdrawsurface7.htm
tech.root: directdraw
ms.assetid: be686d56-c242-4228-ac8e-8f764ad29756
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7, IDirectDrawSurface7 interface [DirectDraw], IDirectDrawSurface7 interface [DirectDraw],described, ddraw/IDirectDrawSurface7, directdraw.idirectdrawsurface7
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
 - IDirectDrawSurface7
 - ddraw/IDirectDrawSurface7
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
 - IDirectDrawSurface7
---

# IDirectDrawSurface7 interface


## -description

Applications use the methods of the <b>IDirectDrawSurface7</b> interface to create DirectDrawSurface objects and work with system-level variables. This section is a reference to the methods of this interface.

## -inheritance

The <b>IDirectDrawSurface7</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawSurface7</b> also has these types of members:

## -remarks

The methods of the <b>IDirectDrawSurface7</b> interface can be organized into the following groups:<table>
<tr>
<th>Group</th>
<th>Methods</th>
</tr>
<tr>
<td>Allocating memory</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-initialize">Initialize</a>,  
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-islost">IsLost</a>,  
and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-restore">Restore</a>
</td>
</tr>
<tr>
<td>Attaching surfaces </td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-addattachedsurface">AddAttachedSurface</a>,  
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-deleteattachedsurface">DeleteAttachedSurface</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-enumattachedsurfaces">EnumAttachedSurfaces</a>,  
and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getattachedsurface">GetAttachedSurface</a>
</td>
</tr>
<tr>
<td>BitBltting</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-blt">Blt</a>,  
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltbatch">BltBatch</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltfast">BltFast</a>,  
 and  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getbltstatus">GetBltStatus</a>
</td>
</tr>
<tr>
<td>Color keying</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getcolorkey">GetColorKey</a>  
  and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setcolorkey">SetColorKey</a>
</td>
</tr>
<tr>
<td>Device contexts </td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc">GetDC</a>  
  and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-releasedc">ReleaseDC</a>
</td>
</tr>
<tr>
<td>Flipping</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-flip">Flip</a>  
  and  
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getflipstatus">GetFlipStatus</a>
</td>
</tr>
<tr>
<td>Locking surfaces </td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-lock">Lock</a>,  
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-pagelock">PageLock</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-pageunlock">PageUnlock</a>,  
and  
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-unlock">Unlock</a>
</td>
</tr>
<tr>
<td>Miscellaneous</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getddinterface">GetDDInterface</a>
</td>
</tr>
<tr>
<td>Overlays </td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-addoverlaydirtyrect">AddOverlayDirtyRect</a>,  
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-enumoverlayzorders">EnumOverlayZOrders</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition">GetOverlayPosition</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setoverlayposition">SetOverlayPosition</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay">UpdateOverlay</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlaydisplay">UpdateOverlayDisplay</a>,  
and 
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlayzorder">UpdateOverlayZOrder</a>
</td>
</tr>
<tr>
<td>Private surface data</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-freeprivatedata">FreePrivateData</a>, 
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getprivatedata">GetPrivateData</a>, 
and 
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setprivatedata">SetPrivateData</a>
</td>
</tr>
<tr>
<td>Surface capabilities </td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getcaps">GetCaps</a>
</td>
</tr>
<tr>
<td>Surface clipper</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getclipper">GetClipper</a>  
  and 
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setclipper">SetClipper</a>
</td>
</tr>
<tr>
<td>Surface characteristics</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-changeuniquenessvalue">ChangeUniquenessValue</a>, 
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getpixelformat">GetPixelFormat</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getsurfacedesc">GetSurfaceDesc</a>,  
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getuniquenessvalue">GetUniquenessValue</a>, 
and 
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setsurfacedesc">SetSurfaceDesc</a>
</td>
</tr>
<tr>
<td>Surface palettes</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getpalette">GetPalette</a>  
  and 
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setpalette">SetPalette</a>
</td>
</tr>
<tr>
<td>Textures</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getlod">GetLOD</a>, 
  <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getpriority">GetPriority</a>, 
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setlod">SetLOD</a>, 
and 
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setpriority">SetPriority</a>
</td>
</tr>
</table>
 



The <b>IDirectDrawSurface7</b> interface extends the features of previous versions of the interface by offering methods that offer better surface management and ease of use. Many methods in this interface accept slightly different parameters than their counterparts in former versions of the interface. Wherever an <b>IDirectDrawSurface3</b> interface method might accept a <a href="/windows/win32/api/ddraw/ns-ddraw-ddsurfacedesc">DDSURFACEDESC</a> structure or an <b>IDirectDrawSurface3</b> interface, the methods in IDirectDrawSurface7 accept a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure or an <b>IDirectDrawSurface7</b> interface, instead.



Use the LPDIRECTDRAWSURFACE, LPDIRECTDRAWSURFACE2, LPDIRECTDRAWSURFACE3, LPDIRECTDRAWSURFACE4, or LPDIRECTDRAWSURFACE7 data type to declare a variable that points to various DirectDrawSurface object interfaces. The Ddraw.h header file declares these data types with the following code:




```

typedef struct IDirectDrawSurface     FAR *LPDIRECTDRAWSURFACE;
typedef struct IDirectDrawSurface2    FAR *LPDIRECTDRAWSURFACE2;
typedef struct IDirectDrawSurface3    FAR *LPDIRECTDRAWSURFACE3;
typedef struct IDirectDrawSurface4    FAR *LPDIRECTDRAWSURFACE4;
typedef struct IDirectDrawSurface7    FAR *LPDIRECTDRAWSURFACE7;

```
