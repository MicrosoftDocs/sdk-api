---
UID: NN:ddraw.IDirectDrawSurface7
title: IDirectDrawSurface7 (ddraw.h)
author: windows-sdk-content
description: Applications use the methods of the IDirectDrawSurface7 interface to create DirectDrawSurface objects and work with system-level variables. This section is a reference to the methods of this interface.
old-location: directdraw\idirectdrawsurface7.htm
tech.root: directdraw
ms.assetid: be686d56-c242-4228-ac8e-8f764ad29756
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7, IDirectDrawSurface7 interface [DirectDraw], IDirectDrawSurface7 interface [DirectDraw],described, ddraw/IDirectDrawSurface7, directdraw.idirectdrawsurface7
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7 interface


## -description


Applications use the methods of the <b>IDirectDrawSurface7</b> interface to create DirectDrawSurface objects and work with system-level variables. This section is a reference to the methods of this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawSurface7</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectDrawSurface7</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6d42c5ed-7f05-4450-b1f4-cb9ee6efa7d9">AddAttachedSurface</a>
</td>
<td align="left" width="63%">
Attaches the specified z-buffer surface to this surface.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ddd02ff-9e7f-4962-8954-0032f23959cd">AddOverlayDirtyRect</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/4ddd02ff-9e7f-4962-8954-0032f23959cd">IDirectDrawSurface7::AddOverlayDirtyRect</a> method is not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e458c430-855c-419b-aa50-144d2b422e78">Blt</a>
</td>
<td align="left" width="63%">
Performs a bit block transfer (bitblt). This method does not support z-buffering or alpha blending during bitblt operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50c071a6-2963-474e-994e-c789b1924d92">BltBatch</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/50c071a6-2963-474e-994e-c789b1924d92">IDirectDrawSurface7::BltBatch</a> method is not currently implemented.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac882b48-87b2-4b65-99b0-ac9065b5f47f">BltFast</a>
</td>
<td align="left" width="63%">
Performs a source copy bitblt or transparent bitblt by using a source color key or destination color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d714fb7-7e12-45ab-ae40-7fc2a65b9e7e">ChangeUniquenessValue</a>
</td>
<td align="left" width="63%">
Manually updates the uniqueness value for this surface.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39cefecd-2ae0-42ba-8140-842acdaa1ad8">DeleteAttachedSurface</a>
</td>
<td align="left" width="63%">
Detaches one or more attached surfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f8e9b53-3aff-491c-ab0c-2f414d1ddb27">EnumAttachedSurfaces</a>
</td>
<td align="left" width="63%">
Enumerates all the surfaces that are attached to this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fab3212c-c1af-4119-85ff-108594cc64fa">EnumOverlayZOrders</a>
</td>
<td align="left" width="63%">
Enumerates the overlay surfaces on the specified destination. You can enumerate the overlays in front-to-back or back-to-front order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c0c23e7-7567-4e07-9ba0-5e50b758f711">Flip</a>
</td>
<td align="left" width="63%">
Makes the surface memory that is associated with the DDSCAPS_BACKBUFFER surface become associated with the front-buffer surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66d3f701-735c-4dca-b7b6-47a17d63c23e">FreePrivateData</a>
</td>
<td align="left" width="63%">
Frees the specified private data that is associated with this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0eae7e55-5ff7-41f6-ac6a-ce7fb6d809b9">GetAttachedSurface</a>
</td>
<td align="left" width="63%">
Obtains the attached surface that has the specified capabilities, and increments the reference count of the retrieved interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f446300-065b-47c1-9778-fb4a5b2ea4bd">GetBltStatus</a>
</td>
<td align="left" width="63%">
Obtains status about a bit block transfer (bitblt) operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/971290b7-7df6-41c7-8197-b6169ddd092b">GetCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of this surface. These capabilities are not necessarily related to the capabilities of the display device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2156dbe-88b5-4ab1-a310-13a38ebdbb4b">GetClipper</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDrawClipper object that is associated with this surface, and increments the reference count of the returned clipper.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0df14c63-f962-4823-873a-3fe1d626f4cb">GetColorKey</a>
</td>
<td align="left" width="63%">
Retrieves the color key value for this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/683be1bc-8232-42de-907f-1136ffdd524d">GetDC</a>
</td>
<td align="left" width="63%">
Creates a GDI-compatible handle of a device context for this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ec63614-cdc0-4d07-97e3-97167e7b397c">GetDDInterface</a>
</td>
<td align="left" width="63%">
Retrieves an interface to the DirectDraw object that was used to create this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e337bdde-bf63-414a-88a5-507478476667">GetFlipStatus</a>
</td>
<td align="left" width="63%">
Retrieves status about whether this surface has finished its flipping process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9208372b-47ac-4079-9e4a-28cf51912a93">GetLOD</a>
</td>
<td align="left" width="63%">
Retrieves the maximum level of detail (LOD) currently set for a managed mipmap surface. This method succeeds only on managed textures.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/008502f7-468f-4d79-a309-75ebdbe29ff3">GetOverlayPosition</a>
</td>
<td align="left" width="63%">
Retrieves the display coordinates of this surface. This method is used on a visible, active overlay surface (that is, a surface that has the DDSCAPS_OVERLAY flag set).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35a667aa-9a69-4c71-9e26-b42359815a0d">GetPalette</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDrawPalette object that is associated with this surface, and increments the reference count of the returned palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c33c46b-6cd7-4ee7-976c-a81f9d92b379">GetPixelFormat</a>
</td>
<td align="left" width="63%">
Retrieves the color and pixel format of this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59a47305-92d5-42a3-9ad1-11c80e3744df">GetPriority</a>
</td>
<td align="left" width="63%">
Retrieves the texture-management priority for this texture. This method succeeds only on managed textures.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8c0c882-329f-4cce-8cd0-ff71c18b1716">GetPrivateData</a>
</td>
<td align="left" width="63%">
Copies the private data that is associated with this surface to a provided buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c36685e-8eb7-4d91-a479-8f099d5e712b">GetSurfaceDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of this surface in its current condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/559d9381-1135-47de-9bbe-49aa8d97f5d3">GetUniquenessValue</a>
</td>
<td align="left" width="63%">
Retrieves the current uniqueness value for this surface.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98b9a05f-ff61-4c58-9c09-625077eb64ad">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a DirectDrawSurface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4654478-ca09-4856-8221-ef5454c23535">IsLost</a>
</td>
<td align="left" width="63%">
Determines whether the surface memory that is associated with a DirectDrawSurface object has been freed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0267ad70-e7cc-41e8-8325-7ede4a662d13">Lock</a>
</td>
<td align="left" width="63%">
Obtains a pointer to the surface memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/018e6539-bb2a-472c-bab4-2c0665cdbe15">PageLock</a>
</td>
<td align="left" width="63%">
Prevents a system-memory surface from being paged out while a bit block transfer (bitblt) operation that uses direct memory access (DMA) transfers to or from system memory is in progress.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a87df37-a53f-4240-a5cb-47b13999c34b">PageUnlock</a>
</td>
<td align="left" width="63%">
Unlocks a system-memory surface, which then allows it to be paged out.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/170d5194-9327-4632-a87f-39aa8a0ccf74">ReleaseDC</a>
</td>
<td align="left" width="63%">
Releases the handle of a device context that was previously obtained by using the <a href="https://msdn.microsoft.com/683be1bc-8232-42de-907f-1136ffdd524d">IDirectDrawSurface7::GetDC</a> method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ca7abb2-5b9a-4323-9f0b-952e183e794b">Restore</a>
</td>
<td align="left" width="63%">
Restores a surface that has been lost. This occurs when the surface memory that is associated with the DirectDrawSurface object has been freed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18bc8018-b00c-40ef-a54a-e2eecdb835a9">SetClipper</a>
</td>
<td align="left" width="63%">
Attaches a clipper object to, or deletes one from, this surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36f2510e-d12a-40af-b65c-aa36ce46a942">SetColorKey</a>
</td>
<td align="left" width="63%">
Sets the color key value for the DirectDrawSurface object if the hardware supports color keys on a per-surface basis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/596b700f-9a16-4ed0-9ea8-8a1da7d841ae">SetLOD</a>
</td>
<td align="left" width="63%">
Sets the maximum level of detail (LOD) for a managed mipmap surface. This method succeeds only on managed textures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94bd79f8-ded2-4cfa-98c1-a03202d3e678">SetOverlayPosition</a>
</td>
<td align="left" width="63%">
Changes the display coordinates of an overlay surface.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/938906fe-9f5b-468b-8b34-5de16aeb67b3">SetPalette</a>
</td>
<td align="left" width="63%">
Attaches a palette object to (or detaches one from) a surface. The surface uses this palette for all subsequent operations. The palette change takes place immediately, without regard to refresh timing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06ab2190-db76-41e5-915e-32a3613505a5">SetPriority</a>
</td>
<td align="left" width="63%">
Assigns the texture-management priority for this texture. This method succeeds only on managed textures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/822e4533-9073-4590-844e-8830110e4e33">SetPrivateData</a>
</td>
<td align="left" width="63%">
Associates data with the surface that is intended for use by the application, not by DirectDraw. Data is passed by value, and multiple sets of data can be associated with a single surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/541bd833-20c4-4b47-a3ed-c29f228a0626">SetSurfaceDesc</a>
</td>
<td align="left" width="63%">
Sets the characteristics of an existing surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1606869a-83b1-4278-a0b5-c183cc7ea285">Unlock</a>
</td>
<td align="left" width="63%">
Notifies DirectDraw that the direct surface manipulations are complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8706c6ca-cd17-490a-8ff9-9470a7d7a150">UpdateOverlay</a>
</td>
<td align="left" width="63%">
Repositions or modifies the visual attributes of an overlay surface. These surfaces must have the DDSCAPS_OVERLAY flag set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50edf36f-ddf2-44a4-bcab-4b4dd5c5b65c">UpdateOverlayDisplay</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/50edf36f-ddf2-44a4-bcab-4b4dd5c5b65c">IDirectDrawSurface7::UpdateOverlayDisplay</a> method is not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a95f315f-7a1f-4ca0-bb18-9bd54f2cc78d">UpdateOverlayZOrder</a>
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
<a href="https://msdn.microsoft.com/98b9a05f-ff61-4c58-9c09-625077eb64ad">Initialize</a>,  
  <a href="https://msdn.microsoft.com/f4654478-ca09-4856-8221-ef5454c23535">IsLost</a>,  
and <a href="https://msdn.microsoft.com/9ca7abb2-5b9a-4323-9f0b-952e183e794b">Restore</a>
</td>
</tr>
<tr>
<td>Attaching surfaces </td>
<td>
<a href="https://msdn.microsoft.com/6d42c5ed-7f05-4450-b1f4-cb9ee6efa7d9">AddAttachedSurface</a>,  
  <a href="https://msdn.microsoft.com/39cefecd-2ae0-42ba-8140-842acdaa1ad8">DeleteAttachedSurface</a>,  
<a href="https://msdn.microsoft.com/7f8e9b53-3aff-491c-ab0c-2f414d1ddb27">EnumAttachedSurfaces</a>,  
and <a href="https://msdn.microsoft.com/0eae7e55-5ff7-41f6-ac6a-ce7fb6d809b9">GetAttachedSurface</a>
</td>
</tr>
<tr>
<td>BitBltting</td>
<td>
<a href="https://msdn.microsoft.com/e458c430-855c-419b-aa50-144d2b422e78">Blt</a>,  
  <a href="https://msdn.microsoft.com/50c071a6-2963-474e-994e-c789b1924d92">BltBatch</a>,  
<a href="https://msdn.microsoft.com/ac882b48-87b2-4b65-99b0-ac9065b5f47f">BltFast</a>,  
 and  
<a href="https://msdn.microsoft.com/1f446300-065b-47c1-9778-fb4a5b2ea4bd">GetBltStatus</a>
</td>
</tr>
<tr>
<td>Color keying</td>
<td>
<a href="https://msdn.microsoft.com/0df14c63-f962-4823-873a-3fe1d626f4cb">GetColorKey</a>  
  and <a href="https://msdn.microsoft.com/36f2510e-d12a-40af-b65c-aa36ce46a942">SetColorKey</a>
</td>
</tr>
<tr>
<td>Device contexts </td>
<td>
<a href="https://msdn.microsoft.com/683be1bc-8232-42de-907f-1136ffdd524d">GetDC</a>  
  and <a href="https://msdn.microsoft.com/170d5194-9327-4632-a87f-39aa8a0ccf74">ReleaseDC</a>
</td>
</tr>
<tr>
<td>Flipping</td>
<td>
<a href="https://msdn.microsoft.com/6c0c23e7-7567-4e07-9ba0-5e50b758f711">Flip</a>  
  and  
  <a href="https://msdn.microsoft.com/e337bdde-bf63-414a-88a5-507478476667">GetFlipStatus</a>
</td>
</tr>
<tr>
<td>Locking surfaces </td>
<td>
<a href="https://msdn.microsoft.com/0267ad70-e7cc-41e8-8325-7ede4a662d13">Lock</a>,  
  <a href="https://msdn.microsoft.com/018e6539-bb2a-472c-bab4-2c0665cdbe15">PageLock</a>,  
<a href="https://msdn.microsoft.com/1a87df37-a53f-4240-a5cb-47b13999c34b">PageUnlock</a>,  
and  
  <a href="https://msdn.microsoft.com/1606869a-83b1-4278-a0b5-c183cc7ea285">Unlock</a>
</td>
</tr>
<tr>
<td>Miscellaneous</td>
<td>
<a href="https://msdn.microsoft.com/1ec63614-cdc0-4d07-97e3-97167e7b397c">GetDDInterface</a>
</td>
</tr>
<tr>
<td>Overlays </td>
<td>
<a href="https://msdn.microsoft.com/4ddd02ff-9e7f-4962-8954-0032f23959cd">AddOverlayDirtyRect</a>,  
  <a href="https://msdn.microsoft.com/fab3212c-c1af-4119-85ff-108594cc64fa">EnumOverlayZOrders</a>,  
<a href="https://msdn.microsoft.com/008502f7-468f-4d79-a309-75ebdbe29ff3">GetOverlayPosition</a>,  
<a href="https://msdn.microsoft.com/94bd79f8-ded2-4cfa-98c1-a03202d3e678">SetOverlayPosition</a>,  
<a href="https://msdn.microsoft.com/8706c6ca-cd17-490a-8ff9-9470a7d7a150">UpdateOverlay</a>,  
<a href="https://msdn.microsoft.com/50edf36f-ddf2-44a4-bcab-4b4dd5c5b65c">UpdateOverlayDisplay</a>,  
and 
<a href="https://msdn.microsoft.com/a95f315f-7a1f-4ca0-bb18-9bd54f2cc78d">UpdateOverlayZOrder</a>
</td>
</tr>
<tr>
<td>Private surface data</td>
<td>
<a href="https://msdn.microsoft.com/66d3f701-735c-4dca-b7b6-47a17d63c23e">FreePrivateData</a>, 
  <a href="https://msdn.microsoft.com/f8c0c882-329f-4cce-8cd0-ff71c18b1716">GetPrivateData</a>, 
and 
<a href="https://msdn.microsoft.com/822e4533-9073-4590-844e-8830110e4e33">SetPrivateData</a>
</td>
</tr>
<tr>
<td>Surface capabilities </td>
<td>
<a href="https://msdn.microsoft.com/4e93612c-9e28-4d51-a640-e8e9b5ed8e7a">GetCaps</a>
</td>
</tr>
<tr>
<td>Surface clipper</td>
<td>
<a href="https://msdn.microsoft.com/f2156dbe-88b5-4ab1-a310-13a38ebdbb4b">GetClipper</a>  
  and 
<a href="https://msdn.microsoft.com/18bc8018-b00c-40ef-a54a-e2eecdb835a9">SetClipper</a>
</td>
</tr>
<tr>
<td>Surface characteristics</td>
<td>
<a href="https://msdn.microsoft.com/4d714fb7-7e12-45ab-ae40-7fc2a65b9e7e">ChangeUniquenessValue</a>, 
  <a href="https://msdn.microsoft.com/2c33c46b-6cd7-4ee7-976c-a81f9d92b379">GetPixelFormat</a>,  
<a href="https://msdn.microsoft.com/4c36685e-8eb7-4d91-a479-8f099d5e712b">GetSurfaceDesc</a>,  
<a href="https://msdn.microsoft.com/559d9381-1135-47de-9bbe-49aa8d97f5d3">GetUniquenessValue</a>, 
and 
<a href="https://msdn.microsoft.com/541bd833-20c4-4b47-a3ed-c29f228a0626">SetSurfaceDesc</a>
</td>
</tr>
<tr>
<td>Surface palettes</td>
<td>
<a href="https://msdn.microsoft.com/35a667aa-9a69-4c71-9e26-b42359815a0d">GetPalette</a>  
  and 
<a href="https://msdn.microsoft.com/938906fe-9f5b-468b-8b34-5de16aeb67b3">SetPalette</a>
</td>
</tr>
<tr>
<td>Textures</td>
<td>
<a href="https://msdn.microsoft.com/9208372b-47ac-4079-9e4a-28cf51912a93">GetLOD</a>, 
  <a href="https://msdn.microsoft.com/59a47305-92d5-42a3-9ad1-11c80e3744df">GetPriority</a>, 
<a href="https://msdn.microsoft.com/596b700f-9a16-4ed0-9ea8-8a1da7d841ae">SetLOD</a>, 
and 
<a href="https://msdn.microsoft.com/06ab2190-db76-41e5-915e-32a3613505a5">SetPriority</a>
</td>
</tr>
</table>
 



The <b>IDirectDrawSurface7</b> interface extends the features of previous versions of the interface by offering methods that offer better surface management and ease of use. Many methods in this interface accept slightly different parameters than their counterparts in former versions of the interface. Wherever an <b>IDirectDrawSurface3</b> interface method might accept a <a href="https://msdn.microsoft.com/a88f37bc-b5c0-4bc1-b6ee-30923362c1ca">DDSURFACEDESC</a> structure or an <b>IDirectDrawSurface3</b> interface, the methods in IDirectDrawSurface7 accept a <a href="https://msdn.microsoft.com/507c557f-eb3a-429c-a738-8d715e5d71d3">DDSURFACEDESC2</a> structure or an <b>IDirectDrawSurface7</b> interface, instead.



Use the LPDIRECTDRAWSURFACE, LPDIRECTDRAWSURFACE2, LPDIRECTDRAWSURFACE3, LPDIRECTDRAWSURFACE4, or LPDIRECTDRAWSURFACE7 data type to declare a variable that points to various DirectDrawSurface object interfaces. The Ddraw.h header file declares these data types with the following code:




```

typedef struct IDirectDrawSurface     FAR *LPDIRECTDRAWSURFACE;
typedef struct IDirectDrawSurface2    FAR *LPDIRECTDRAWSURFACE2;
typedef struct IDirectDrawSurface3    FAR *LPDIRECTDRAWSURFACE3;
typedef struct IDirectDrawSurface4    FAR *LPDIRECTDRAWSURFACE4;
typedef struct IDirectDrawSurface7    FAR *LPDIRECTDRAWSURFACE7;

```




