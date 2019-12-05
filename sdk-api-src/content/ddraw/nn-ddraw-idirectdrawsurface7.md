---
UID: NN:ddraw.IDirectDrawSurface7
title: IDirectDrawSurface7 (ddraw.h)
description: Applications use the methods of the IDirectDrawSurface7 interface to create DirectDrawSurface objects and work with system-level variables. This section is a reference to the methods of this interface.
old-location: directdraw\idirectdrawsurface7.htm
tech.root: directdraw
ms.assetid: be686d56-c242-4228-ac8e-8f764ad29756
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7, IDirectDrawSurface7 interface [DirectDraw], IDirectDrawSurface7 interface [DirectDraw],described, ddraw/IDirectDrawSurface7, directdraw.idirectdrawsurface7
ms.topic: interface
f1_keywords:
- ddraw/IDirectDrawSurface7
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ddraw.dll
api_name:
- IDirectDrawSurface7
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawSurface7 interface


## -description


Applications use the methods of the <b>IDirectDrawSurface7</b> interface to create DirectDrawSurface objects and work with system-level variables. This section is a reference to the methods of this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawSurface7</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawSurface7</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawSurface7</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-addattachedsurface">AddAttachedSurface</a>
</td>
<td align="left" width="63%">
Attaches the specified z-buffer surface to this surface.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-addoverlaydirtyrect">AddOverlayDirtyRect</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-addoverlaydirtyrect">IDirectDrawSurface7::AddOverlayDirtyRect</a> method is not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-blt">Blt</a>
</td>
<td align="left" width="63%">
Performs a bit block transfer (bitblt). This method does not support z-buffering or alpha blending during bitblt operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltbatch">BltBatch</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltbatch">IDirectDrawSurface7::BltBatch</a> method is not currently implemented.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltfast">BltFast</a>
</td>
<td align="left" width="63%">
Performs a source copy bitblt or transparent bitblt by using a source color key or destination color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-changeuniquenessvalue">ChangeUniquenessValue</a>
</td>
<td align="left" width="63%">
Manually updates the uniqueness value for this surface.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-deleteattachedsurface">DeleteAttachedSurface</a>
</td>
<td align="left" width="63%">
Detaches one or more attached surfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-enumattachedsurfaces">EnumAttachedSurfaces</a>
</td>
<td align="left" width="63%">
Enumerates all the surfaces that are attached to this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-enumoverlayzorders">EnumOverlayZOrders</a>
</td>
<td align="left" width="63%">
Enumerates the overlay surfaces on the specified destination. You can enumerate the overlays in front-to-back or back-to-front order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-flip">Flip</a>
</td>
<td align="left" width="63%">
Makes the surface memory that is associated with the DDSCAPS_BACKBUFFER surface become associated with the front-buffer surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-freeprivatedata">FreePrivateData</a>
</td>
<td align="left" width="63%">
Frees the specified private data that is associated with this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getattachedsurface">GetAttachedSurface</a>
</td>
<td align="left" width="63%">
Obtains the attached surface that has the specified capabilities, and increments the reference count of the retrieved interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getbltstatus">GetBltStatus</a>
</td>
<td align="left" width="63%">
Obtains status about a bit block transfer (bitblt) operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getcaps">GetCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of this surface. These capabilities are not necessarily related to the capabilities of the display device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getclipper">GetClipper</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDrawClipper object that is associated with this surface, and increments the reference count of the returned clipper.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getcolorkey">GetColorKey</a>
</td>
<td align="left" width="63%">
Retrieves the color key value for this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc">GetDC</a>
</td>
<td align="left" width="63%">
Creates a GDI-compatible handle of a device context for this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getddinterface">GetDDInterface</a>
</td>
<td align="left" width="63%">
Retrieves an interface to the DirectDraw object that was used to create this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getflipstatus">GetFlipStatus</a>
</td>
<td align="left" width="63%">
Retrieves status about whether this surface has finished its flipping process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getlod">GetLOD</a>
</td>
<td align="left" width="63%">
Retrieves the maximum level of detail (LOD) currently set for a managed mipmap surface. This method succeeds only on managed textures.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition">GetOverlayPosition</a>
</td>
<td align="left" width="63%">
Retrieves the display coordinates of this surface. This method is used on a visible, active overlay surface (that is, a surface that has the DDSCAPS_OVERLAY flag set).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getpalette">GetPalette</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDrawPalette object that is associated with this surface, and increments the reference count of the returned palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getpixelformat">GetPixelFormat</a>
</td>
<td align="left" width="63%">
Retrieves the color and pixel format of this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getpriority">GetPriority</a>
</td>
<td align="left" width="63%">
Retrieves the texture-management priority for this texture. This method succeeds only on managed textures.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getprivatedata">GetPrivateData</a>
</td>
<td align="left" width="63%">
Copies the private data that is associated with this surface to a provided buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getsurfacedesc">GetSurfaceDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of this surface in its current condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getuniquenessvalue">GetUniquenessValue</a>
</td>
<td align="left" width="63%">
Retrieves the current uniqueness value for this surface.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a DirectDrawSurface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-islost">IsLost</a>
</td>
<td align="left" width="63%">
Determines whether the surface memory that is associated with a DirectDrawSurface object has been freed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-lock">Lock</a>
</td>
<td align="left" width="63%">
Obtains a pointer to the surface memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-pagelock">PageLock</a>
</td>
<td align="left" width="63%">
Prevents a system-memory surface from being paged out while a bit block transfer (bitblt) operation that uses direct memory access (DMA) transfers to or from system memory is in progress.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-pageunlock">PageUnlock</a>
</td>
<td align="left" width="63%">
Unlocks a system-memory surface, which then allows it to be paged out.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-releasedc">ReleaseDC</a>
</td>
<td align="left" width="63%">
Releases the handle of a device context that was previously obtained by using the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc">IDirectDrawSurface7::GetDC</a> method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-restore">Restore</a>
</td>
<td align="left" width="63%">
Restores a surface that has been lost. This occurs when the surface memory that is associated with the DirectDrawSurface object has been freed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setclipper">SetClipper</a>
</td>
<td align="left" width="63%">
Attaches a clipper object to, or deletes one from, this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setcolorkey">SetColorKey</a>
</td>
<td align="left" width="63%">
Sets the color key value for the DirectDrawSurface object if the hardware supports color keys on a per-surface basis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setlod">SetLOD</a>
</td>
<td align="left" width="63%">
Sets the maximum level of detail (LOD) for a managed mipmap surface. This method succeeds only on managed textures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setoverlayposition">SetOverlayPosition</a>
</td>
<td align="left" width="63%">
Changes the display coordinates of an overlay surface.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setpalette">SetPalette</a>
</td>
<td align="left" width="63%">
Attaches a palette object to (or detaches one from) a surface. The surface uses this palette for all subsequent operations. The palette change takes place immediately, without regard to refresh timing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setpriority">SetPriority</a>
</td>
<td align="left" width="63%">
Assigns the texture-management priority for this texture. This method succeeds only on managed textures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setprivatedata">SetPrivateData</a>
</td>
<td align="left" width="63%">
Associates data with the surface that is intended for use by the application, not by DirectDraw. Data is passed by value, and multiple sets of data can be associated with a single surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setsurfacedesc">SetSurfaceDesc</a>
</td>
<td align="left" width="63%">
Sets the characteristics of an existing surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-unlock">Unlock</a>
</td>
<td align="left" width="63%">
Notifies DirectDraw that the direct surface manipulations are complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay">UpdateOverlay</a>
</td>
<td align="left" width="63%">
Repositions or modifies the visual attributes of an overlay surface. These surfaces must have the DDSCAPS_OVERLAY flag set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlaydisplay">UpdateOverlayDisplay</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlaydisplay">IDirectDrawSurface7::UpdateOverlayDisplay</a> method is not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlayzorder">UpdateOverlayZOrder</a>
</td>
<td align="left" width="63%">
Sets the z-order of an overlay.

</td>
</tr>
</table> 


## -remarks



The methods of the <b>IDirectDrawSurface7</b> interface can be organized into the following groups:<table>
<tr>
<th>Group</th>
<th>Methods</th>
</tr>
<tr>
<td>Allocating memory</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-initialize">Initialize</a>,  
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-islost">IsLost</a>,  
and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-restore">Restore</a>
</td>
</tr>
<tr>
<td>Attaching surfaces </td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-addattachedsurface">AddAttachedSurface</a>,  
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-deleteattachedsurface">DeleteAttachedSurface</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-enumattachedsurfaces">EnumAttachedSurfaces</a>,  
and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getattachedsurface">GetAttachedSurface</a>
</td>
</tr>
<tr>
<td>BitBltting</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-blt">Blt</a>,  
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltbatch">BltBatch</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltfast">BltFast</a>,  
 and  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getbltstatus">GetBltStatus</a>
</td>
</tr>
<tr>
<td>Color keying</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getcolorkey">GetColorKey</a>  
  and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setcolorkey">SetColorKey</a>
</td>
</tr>
<tr>
<td>Device contexts </td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc">GetDC</a>  
  and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-releasedc">ReleaseDC</a>
</td>
</tr>
<tr>
<td>Flipping</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-flip">Flip</a>  
  and  
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getflipstatus">GetFlipStatus</a>
</td>
</tr>
<tr>
<td>Locking surfaces </td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-lock">Lock</a>,  
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-pagelock">PageLock</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-pageunlock">PageUnlock</a>,  
and  
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-unlock">Unlock</a>
</td>
</tr>
<tr>
<td>Miscellaneous</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getddinterface">GetDDInterface</a>
</td>
</tr>
<tr>
<td>Overlays </td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-addoverlaydirtyrect">AddOverlayDirtyRect</a>,  
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-enumoverlayzorders">EnumOverlayZOrders</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition">GetOverlayPosition</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setoverlayposition">SetOverlayPosition</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay">UpdateOverlay</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlaydisplay">UpdateOverlayDisplay</a>,  
and 
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlayzorder">UpdateOverlayZOrder</a>
</td>
</tr>
<tr>
<td>Private surface data</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-freeprivatedata">FreePrivateData</a>, 
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getprivatedata">GetPrivateData</a>, 
and 
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setprivatedata">SetPrivateData</a>
</td>
</tr>
<tr>
<td>Surface capabilities </td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getcaps">GetCaps</a>
</td>
</tr>
<tr>
<td>Surface clipper</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getclipper">GetClipper</a>  
  and 
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setclipper">SetClipper</a>
</td>
</tr>
<tr>
<td>Surface characteristics</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-changeuniquenessvalue">ChangeUniquenessValue</a>, 
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getpixelformat">GetPixelFormat</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getsurfacedesc">GetSurfaceDesc</a>,  
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getuniquenessvalue">GetUniquenessValue</a>, 
and 
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setsurfacedesc">SetSurfaceDesc</a>
</td>
</tr>
<tr>
<td>Surface palettes</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getpalette">GetPalette</a>  
  and 
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setpalette">SetPalette</a>
</td>
</tr>
<tr>
<td>Textures</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getlod">GetLOD</a>, 
  <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getpriority">GetPriority</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setlod">SetLOD</a>, 
and 
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setpriority">SetPriority</a>
</td>
</tr>
</table>
 



The <b>IDirectDrawSurface7</b> interface extends the features of previous versions of the interface by offering methods that offer better surface management and ease of use. Many methods in this interface accept slightly different parameters than their counterparts in former versions of the interface. Wherever an <b>IDirectDrawSurface3</b> interface method might accept a <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)">DDSURFACEDESC</a> structure or an <b>IDirectDrawSurface3</b> interface, the methods in IDirectDrawSurface7 accept a <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure or an <b>IDirectDrawSurface7</b> interface, instead.



Use the LPDIRECTDRAWSURFACE, LPDIRECTDRAWSURFACE2, LPDIRECTDRAWSURFACE3, LPDIRECTDRAWSURFACE4, or LPDIRECTDRAWSURFACE7 data type to declare a variable that points to various DirectDrawSurface object interfaces. The Ddraw.h header file declares these data types with the following code:




```

typedef struct IDirectDrawSurface     FAR *LPDIRECTDRAWSURFACE;
typedef struct IDirectDrawSurface2    FAR *LPDIRECTDRAWSURFACE2;
typedef struct IDirectDrawSurface3    FAR *LPDIRECTDRAWSURFACE3;
typedef struct IDirectDrawSurface4    FAR *LPDIRECTDRAWSURFACE4;
typedef struct IDirectDrawSurface7    FAR *LPDIRECTDRAWSURFACE7;

```




