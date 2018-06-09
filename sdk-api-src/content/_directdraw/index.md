---
UID: TP:directdraw
ms.assetid: 43e6d44d-8b53-399d-b068-b5e0d91fc439
ms.author: windowssdkdev
ms.date: 06/09/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# DirectDraw

## -description

Overview of the DirectDraw technology.

To develop DirectDraw, you need these headers:

 * [ddraw.h](../ddraw/index.md)

For the programming guide, see [DirectDraw](/windows/desktop/directdraw).

## Functions

| Title   | Description   |
| ---- |:---- |
| [DirectDrawCreate function](..\ddraw\nf-ddraw-directdrawcreate.md) | Creates an instance of a DirectDraw object. |
| [DirectDrawCreateClipper function](..\ddraw\nf-ddraw-directdrawcreateclipper.md) | Creates an instance of a DirectDrawClipper object that is not associated with a DirectDraw object. |
| [DirectDrawCreateEx function](..\ddraw\nf-ddraw-directdrawcreateex.md) | Creates an instance of a DirectDraw object that supports the set of Direct3D interfaces in DirectX 7.0. To use the features of Direct3D in DirectX 7.0, create a DirectDraw object with this function. |
| [DirectDrawEnumerateExA function](..\ddraw\nf-ddraw-directdrawenumerateexa.md) | Enumerates all DirectDraw devices that are installed on the computer. The NULL entry always identifies the primary display device that is shared with GDI. |
| [DirectDrawEnumerateExW function](..\ddraw\nf-ddraw-directdrawenumerateexw.md) | Enumerates all DirectDraw devices that are installed on the computer. The NULL entry always identifies the primary display device that is shared with GDI. |
| [DirectDrawEnumerateW function](..\ddraw\nf-ddraw-directdrawenumeratew.md) | This function is superseded by the DirectDrawEnumerateEx function. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [LPDDENUMCALLBACKA callback function](..\ddraw\nc-ddraw-lpddenumcallbacka.md) | The DDEnumCallback function is an application-defined callback function for the DirectDrawEnumerate function. |
| [LPDDENUMCALLBACKEXA callback function](..\ddraw\nc-ddraw-lpddenumcallbackexa.md) | The DDEnumCallbackEx function is an application-defined callback function for the DirectDrawEnumerateEx function. |
| [LPDDENUMCALLBACKEXW callback function](..\ddraw\nc-ddraw-lpddenumcallbackexw.md) | The DDEnumCallbackEx function is an application-defined callback function for the DirectDrawEnumerateEx function. |
| [LPDDENUMCALLBACKW callback function](..\ddraw\nc-ddraw-lpddenumcallbackw.md) | The DDEnumCallback function is an application-defined callback function for the DirectDrawEnumerate function. |
| [LPDDENUMMODESCALLBACK callback function](..\ddraw\nc-ddraw-lpddenummodescallback.md) | Do not use. This callback function is superseded by the EnumModesCallback2 function that is used with the IDirectDraw7 |
| [LPDDENUMMODESCALLBACK2 callback function](..\ddraw\nc-ddraw-lpddenummodescallback2.md) | The EnumModesCallback2 function is an application-defined callback function for the IDirectDraw7 |
| [LPDDENUMSURFACESCALLBACK callback function](..\ddraw\nc-ddraw-lpddenumsurfacescallback.md) | Do not use. This callback function is superseded by the EnumSurfacesCallback7 function that is used with the IDirectDraw7 |
| [LPDDENUMSURFACESCALLBACK2 callback function](..\ddraw\nc-ddraw-lpddenumsurfacescallback2.md) | Do not use. This callback function is superseded by the EnumSurfacesCallback7 function that is used with the IDirectDraw7 |
| [LPDDENUMSURFACESCALLBACK7 callback function](..\ddraw\nc-ddraw-lpddenumsurfacescallback7.md) | The EnumSurfacesCallback7 function is an application-defined callback function for the IDirectDrawSurface7 |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_DDBLTBATCH structure](..\ddraw\ns-ddraw-_ddbltbatch.md) | The DDBLTBATCH structure passes bit block transfer (bitblt) operations to the IDirectDrawSurface7 |
| [_DDBLTFX structure](..\ddraw\ns-ddraw-_ddbltfx.md) | The DDBLTFX structure passes raster operations (ROPs), effects, and override information to the IDirectDrawSurface7 |
| [_DDCAPS_DX3 structure](..\ddraw\ns-ddraw-_ddcaps_dx3.md) | The DDCAPS structure represents the capabilities of the hardware exposed through the DirectDraw object. |
| [_DDCAPS_DX5 structure](..\ddraw\ns-ddraw-_ddcaps_dx5.md) | The DDCAPS structure represents the capabilities of the hardware exposed through the DirectDraw object. |
| [_DDCAPS_DX6 structure](..\ddraw\ns-ddraw-_ddcaps_dx6.md) | The DDCAPS structure represents the capabilities of the hardware exposed through the DirectDraw object. |
| [_DDCAPS_DX7 structure](..\ddraw\ns-ddraw-_ddcaps_dx7.md) | The DDCAPS structure represents the capabilities of the hardware exposed through the DirectDraw object. |
| [_DDCOLORCONTROL structure](..\ddraw\ns-ddraw-_ddcolorcontrol.md) | The DDCOLORCONTROL structure defines the color controls that are associated with an overlay surface or a primary surface. |
| [_DDCOLORKEY structure](..\ddraw\ns-ddraw-_ddcolorkey.md) | The DDCOLORKEY structure describes a source color key, destination color key, or color space. |
| [_DDGAMMARAMP structure](..\ddraw\ns-ddraw-_ddgammaramp.md) | The DDGAMMARAMP structure contains red, green, and blue ramp data for the IDirectDrawGammaControl |
| [_DDOVERLAYFX structure](..\ddraw\ns-ddraw-_ddoverlayfx.md) | The DDOVERLAYFX structure passes overlay information to the IDirectDrawSurface7 |
| [_DDPIXELFORMAT structure](..\ddraw\ns-ddraw-_ddpixelformat.md) | The DDPIXELFORMAT structure describes the pixel format of a DirectDrawSurface object for the IDirectDrawSurface7 |
| [_DDSCAPS structure](..\ddraw\ns-ddraw-_ddscaps.md) | The DDSCAPS structure defines the capabilities of a DirectDrawSurface object. This structure is part of the DDCAPS and DDSURFACEDESC structures. |
| [_DDSCAPS2 structure](..\ddraw\ns-ddraw-_ddscaps2.md) | The DDSCAPS2 structure defines the capabilities of a DirectDrawSurface object. This structure is part of the DDSURFACEDESC2 structure. |
| [_DDSURFACEDESC structure](..\ddraw\ns-ddraw-_ddsurfacedesc.md) | Do not use. This structure is superseded by the DDSURFACEDESC2 structure that is used with the IDirectDraw7 and IDirectDrawSurface7 interfaces. |
| [_DDSURFACEDESC2 structure](..\ddraw\ns-ddraw-_ddsurfacedesc2.md) | The DDSURFACEDESC2 structure contains a description of a surface. |
| [tagDDDEVICEIDENTIFIER2 structure](..\ddraw\ns-ddraw-tagdddeviceidentifier2.md) | The DDDEVICEIDENTIFIER2 structure is passed to the IDirectDraw7 |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IDirectDraw7 interface](..\ddraw\nn-ddraw-idirectdraw7.md) | Applications use the methods of the IDirectDraw7 interface to create DirectDraw objects and work with system-level variables. This section is a reference to the methods of the IDirectDraw7 interface. |
| [IDirectDrawClipper interface](..\ddraw\nn-ddraw-idirectdrawclipper.md) | Applications use the methods of the IDirectDrawClipper interface to manage clip lists. This section is a reference to the methods of this interface. |
| [IDirectDrawColorControl interface](..\ddraw\nn-ddraw-idirectdrawcolorcontrol.md) | Applications use the methods of the IDirectDrawColorControl interface to get and set color controls. |
| [IDirectDrawGammaControl interface](..\ddraw\nn-ddraw-idirectdrawgammacontrol.md) | Applications use the methods of the IDirectDrawGammaControl interface to adjust the red, green, and blue gamma ramp levels of the primary surface. This section is a reference to the methods of this interface. |
| [IDirectDrawPalette interface](..\ddraw\nn-ddraw-idirectdrawpalette.md) | Applications use the methods of the IDirectDrawPalette interface to create DirectDrawPalette objects and work with system-level variables. This section is a reference to the methods of this interface. |
| [IDirectDrawSurface7 interface](..\ddraw\nn-ddraw-idirectdrawsurface7.md) | Applications use the methods of the IDirectDrawSurface7 interface to create DirectDrawSurface objects and work with system-level variables. This section is a reference to the methods of this interface. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IDirectDraw7::Compact](..\ddraw\nf-ddraw-idirectdraw7-compact.md) | This method is not currently implemented. |
| [IDirectDraw7::CreateClipper](..\ddraw\nf-ddraw-idirectdraw7-createclipper.md) | Creates a DirectDrawClipper object. |
| [IDirectDraw7::CreatePalette](..\ddraw\nf-ddraw-idirectdraw7-createpalette.md) | Creates a DirectDrawPalette object for this DirectDraw object. |
| [IDirectDraw7::CreateSurface](..\ddraw\nf-ddraw-idirectdraw7-createsurface.md) | Creates a DirectDrawSurface object for this DirectDraw object. |
| [IDirectDraw7::DuplicateSurface](..\ddraw\nf-ddraw-idirectdraw7-duplicatesurface.md) | Duplicates a DirectDrawSurface object. |
| [IDirectDraw7::EnumDisplayModes](..\ddraw\nf-ddraw-idirectdraw7-enumdisplaymodes.md) | Enumerates all the display modes that the hardware exposes through the DirectDraw object and that are compatible with a provided surface description. |
| [IDirectDraw7::EnumSurfaces](..\ddraw\nf-ddraw-idirectdraw7-enumsurfaces.md) | Enumerates all the existing or possible surfaces that meet the specified surface description. |
| [IDirectDraw7::EvaluateMode](..\ddraw\nf-ddraw-idirectdraw7-evaluatemode.md) | Used after a call to IDirectDraw7 |
| [IDirectDraw7::FlipToGDISurface](..\ddraw\nf-ddraw-idirectdraw7-fliptogdisurface.md) | Makes the surface that the GDI writes to the primary surface. |
| [IDirectDraw7::GetAvailableVidMem](..\ddraw\nf-ddraw-idirectdraw7-getavailablevidmem.md) | Retrieves the total amount of display memory available and the amount of display memory currently free for a given type of surface. |
| [IDirectDraw7::GetCaps](..\ddraw\nf-ddraw-idirectdraw7-getcaps.md) | Retrieves the capabilities of the device driver for the hardware and the hardware emulation layer (HEL). |
| [IDirectDraw7::GetDeviceIdentifier](..\ddraw\nf-ddraw-idirectdraw7-getdeviceidentifier.md) | Obtains information about the device driver. This method can be used, with caution, to recognize specific hardware installations to implement workarounds for poor driver or chipset behavior. |
| [IDirectDraw7::GetDisplayMode](..\ddraw\nf-ddraw-idirectdraw7-getdisplaymode.md) | Retrieves the current display mode. |
| [IDirectDraw7::GetFourCCCodes](..\ddraw\nf-ddraw-idirectdraw7-getfourcccodes.md) | Retrieves the four-character codes (FOURCC) that are supported by the DirectDraw object. This method can also retrieve the number of codes that are supported. |
| [IDirectDraw7::GetGDISurface](..\ddraw\nf-ddraw-idirectdraw7-getgdisurface.md) | Retrieves the DirectDrawSurface object that currently represents the surface memory that GDI is treating as the primary surface. |
| [IDirectDraw7::GetMonitorFrequency](..\ddraw\nf-ddraw-idirectdraw7-getmonitorfrequency.md) | Retrieves the frequency of the monitor that the DirectDraw object controls. |
| [IDirectDraw7::GetScanLine](..\ddraw\nf-ddraw-idirectdraw7-getscanline.md) | Retrieves the scan line that is currently being drawn on the monitor. |
| [IDirectDraw7::GetSurfaceFromDC](..\ddraw\nf-ddraw-idirectdraw7-getsurfacefromdc.md) | Retrieves the IDirectDrawSurface7 interface for a surface, based on its GDI device context handle. |
| [IDirectDraw7::GetVerticalBlankStatus](..\ddraw\nf-ddraw-idirectdraw7-getverticalblankstatus.md) | Retrieves the status of the vertical blank. |
| [IDirectDraw7::Initialize](..\ddraw\nf-ddraw-idirectdraw7-initialize.md) | Initializes a DirectDraw object that was created by using the CoCreateInstance COM function. |
| [IDirectDraw7::RestoreAllSurfaces](..\ddraw\nf-ddraw-idirectdraw7-restoreallsurfaces.md) | Restores all the surfaces that were created for the DirectDraw object, in the order that they were created. |
| [IDirectDraw7::RestoreDisplayMode](..\ddraw\nf-ddraw-idirectdraw7-restoredisplaymode.md) | Resets the mode of the display device hardware for the primary surface to what it was before the IDirectDraw7 |
| [IDirectDraw7::SetCooperativeLevel](..\ddraw\nf-ddraw-idirectdraw7-setcooperativelevel.md) | Determines the top-level behavior of the application. |
| [IDirectDraw7::SetDisplayMode](..\ddraw\nf-ddraw-idirectdraw7-setdisplaymode.md) | Sets the mode of the display-device hardware. |
| [IDirectDraw7::StartModeTest](..\ddraw\nf-ddraw-idirectdraw7-startmodetest.md) | Initiates a test to update the system registry with refresh rate information for the current display adapter and monitor combination. |
| [IDirectDraw7::TestCooperativeLevel](..\ddraw\nf-ddraw-idirectdraw7-testcooperativelevel.md) | Reports the current cooperative-level status of the DirectDraw device for a windowed or full-screen application. |
| [IDirectDraw7::WaitForVerticalBlank](..\ddraw\nf-ddraw-idirectdraw7-waitforverticalblank.md) | Helps the application synchronize itself with the vertical-blank interval. |
| [IDirectDrawClipper::GetClipList](..\ddraw\nf-ddraw-idirectdrawclipper-getcliplist.md) | Retrieves a copy of the clip list that is associated with a DirectDrawClipper object. To select a subset of the clip list, you can pass a rectangle that clips the clip list. |
| [IDirectDrawClipper::GetHWnd](..\ddraw\nf-ddraw-idirectdrawclipper-gethwnd.md) | Retrieves the window handle that was previously associated with this DirectDrawClipper object by the IDirectDrawClipper |
| [IDirectDrawClipper::Initialize](..\ddraw\nf-ddraw-idirectdrawclipper-initialize.md) | Initializes a DirectDrawClipper object that was created by using the CoCreateInstance COM function. |
| [IDirectDrawClipper::IsClipListChanged](..\ddraw\nf-ddraw-idirectdrawclipper-iscliplistchanged.md) | Retrieves the status of the clip list if a window handle is associated with a DirectDrawClipper object. |
| [IDirectDrawClipper::SetClipList](..\ddraw\nf-ddraw-idirectdrawclipper-setcliplist.md) | Sets or deletes the clip list that is used by the IDirectDrawSurface7 |
| [IDirectDrawClipper::SetHWnd](..\ddraw\nf-ddraw-idirectdrawclipper-sethwnd.md) | Sets the window handle that the clipper object uses to obtain clipping information. |
| [IDirectDrawColorControl::GetColorControls](..\ddraw\nf-ddraw-idirectdrawcolorcontrol-getcolorcontrols.md) | Retrieves the current color-control settings that are associated with an overlay or a primary surface. |
| [IDirectDrawColorControl::SetColorControls](..\ddraw\nf-ddraw-idirectdrawcolorcontrol-setcolorcontrols.md) | Sets the color-control options for an overlay or a primary surface. |
| [IDirectDrawGammaControl::GetGammaRamp](..\ddraw\nf-ddraw-idirectdrawgammacontrol-getgammaramp.md) | Retrieves the red, green, and blue gamma ramps for the primary surface. |
| [IDirectDrawGammaControl::SetGammaRamp](..\ddraw\nf-ddraw-idirectdrawgammacontrol-setgammaramp.md) | Sets the red, green, and blue gamma ramps for the primary surface. |
| [IDirectDrawPalette::GetCaps](..\ddraw\nf-ddraw-idirectdrawpalette-getcaps.md) | Retrieves the capabilities of the palette object. |
| [IDirectDrawPalette::GetEntries](..\ddraw\nf-ddraw-idirectdrawpalette-getentries.md) | Retrieves palette values from a DirectDrawPalette object. |
| [IDirectDrawPalette::Initialize](..\ddraw\nf-ddraw-idirectdrawpalette-initialize.md) | Initializes the DirectDrawPalette object. |
| [IDirectDrawPalette::SetEntries](..\ddraw\nf-ddraw-idirectdrawpalette-setentries.md) | Changes entries in a DirectDrawPalette object immediately. |
| [IDirectDrawSurface7::AddAttachedSurface](..\ddraw\nf-ddraw-idirectdrawsurface7-addattachedsurface.md) | Attaches the specified z-buffer surface to this surface. |
| [IDirectDrawSurface7::AddOverlayDirtyRect](..\ddraw\nf-ddraw-idirectdrawsurface7-addoverlaydirtyrect.md) | The IDirectDrawSurface7 |
| [IDirectDrawSurface7::BltBatch](..\ddraw\nf-ddraw-idirectdrawsurface7-bltbatch.md) | The IDirectDrawSurface7 |
| [IDirectDrawSurface7::BltFast](..\ddraw\nf-ddraw-idirectdrawsurface7-bltfast.md) | Performs a source copy bitblt or transparent bitblt by using a source color key or destination color key. |
| [IDirectDrawSurface7::Blt](..\ddraw\nf-ddraw-idirectdrawsurface7-blt.md) | Performs a bit block transfer (bitblt). This method does not support z-buffering or alpha blending during bitblt operations. |
| [IDirectDrawSurface7::ChangeUniquenessValue](..\ddraw\nf-ddraw-idirectdrawsurface7-changeuniquenessvalue.md) | Manually updates the uniqueness value for this surface. |
| [IDirectDrawSurface7::DeleteAttachedSurface](..\ddraw\nf-ddraw-idirectdrawsurface7-deleteattachedsurface.md) | Detaches one or more attached surfaces. |
| [IDirectDrawSurface7::EnumAttachedSurfaces](..\ddraw\nf-ddraw-idirectdrawsurface7-enumattachedsurfaces.md) | Enumerates all the surfaces that are attached to this surface. |
| [IDirectDrawSurface7::EnumOverlayZOrders](..\ddraw\nf-ddraw-idirectdrawsurface7-enumoverlayzorders.md) | Enumerates the overlay surfaces on the specified destination. You can enumerate the overlays in front-to-back or back-to-front order. |
| [IDirectDrawSurface7::Flip](..\ddraw\nf-ddraw-idirectdrawsurface7-flip.md) | Makes the surface memory that is associated with the DDSCAPS_BACKBUFFER surface become associated with the front-buffer surface. |
| [IDirectDrawSurface7::FreePrivateData](..\ddraw\nf-ddraw-idirectdrawsurface7-freeprivatedata.md) | Frees the specified private data that is associated with this surface. |
| [IDirectDrawSurface7::GetAttachedSurface](..\ddraw\nf-ddraw-idirectdrawsurface7-getattachedsurface.md) | Obtains the attached surface that has the specified capabilities, and increments the reference count of the retrieved interface. |
| [IDirectDrawSurface7::GetBltStatus](..\ddraw\nf-ddraw-idirectdrawsurface7-getbltstatus.md) | Obtains status about a bit block transfer (bitblt) operation. |
| [IDirectDrawSurface7::GetCaps](..\ddraw\nf-ddraw-idirectdrawsurface7-getcaps.md) | Retrieves the capabilities of this surface. These capabilities are not necessarily related to the capabilities of the display device. |
| [IDirectDrawSurface7::GetClipper](..\ddraw\nf-ddraw-idirectdrawsurface7-getclipper.md) | Retrieves the DirectDrawClipper object that is associated with this surface, and increments the reference count of the returned clipper. |
| [IDirectDrawSurface7::GetColorKey](..\ddraw\nf-ddraw-idirectdrawsurface7-getcolorkey.md) | Retrieves the color key value for this surface. |
| [IDirectDrawSurface7::GetDC](..\ddraw\nf-ddraw-idirectdrawsurface7-getdc.md) | Creates a GDI-compatible handle of a device context for this surface. |
| [IDirectDrawSurface7::GetDDInterface](..\ddraw\nf-ddraw-idirectdrawsurface7-getddinterface.md) | Retrieves an interface to the DirectDraw object that was used to create this surface. |
| [IDirectDrawSurface7::GetFlipStatus](..\ddraw\nf-ddraw-idirectdrawsurface7-getflipstatus.md) | Retrieves status about whether this surface has finished its flipping process. |
| [IDirectDrawSurface7::GetLOD](..\ddraw\nf-ddraw-idirectdrawsurface7-getlod.md) | Retrieves the maximum level of detail (LOD) currently set for a managed mipmap surface. This method succeeds only on managed textures. |
| [IDirectDrawSurface7::GetOverlayPosition](..\ddraw\nf-ddraw-idirectdrawsurface7-getoverlayposition.md) | Retrieves the display coordinates of this surface. This method is used on a visible, active overlay surface (that is, a surface that has the DDSCAPS_OVERLAY flag set). |
| [IDirectDrawSurface7::GetPalette](..\ddraw\nf-ddraw-idirectdrawsurface7-getpalette.md) | Retrieves the DirectDrawPalette object that is associated with this surface, and increments the reference count of the returned palette. |
| [IDirectDrawSurface7::GetPixelFormat](..\ddraw\nf-ddraw-idirectdrawsurface7-getpixelformat.md) | Retrieves the color and pixel format of this surface. |
| [IDirectDrawSurface7::GetPriority](..\ddraw\nf-ddraw-idirectdrawsurface7-getpriority.md) | Retrieves the texture-management priority for this texture. This method succeeds only on managed textures. |
| [IDirectDrawSurface7::GetPrivateData](..\ddraw\nf-ddraw-idirectdrawsurface7-getprivatedata.md) | Copies the private data that is associated with this surface to a provided buffer. |
| [IDirectDrawSurface7::GetSurfaceDesc](..\ddraw\nf-ddraw-idirectdrawsurface7-getsurfacedesc.md) | Retrieves a description of this surface in its current condition. |
| [IDirectDrawSurface7::GetUniquenessValue](..\ddraw\nf-ddraw-idirectdrawsurface7-getuniquenessvalue.md) | Retrieves the current uniqueness value for this surface. |
| [IDirectDrawSurface7::Initialize](..\ddraw\nf-ddraw-idirectdrawsurface7-initialize.md) | Initializes a DirectDrawSurface object. |
| [IDirectDrawSurface7::IsLost](..\ddraw\nf-ddraw-idirectdrawsurface7-islost.md) | Determines whether the surface memory that is associated with a DirectDrawSurface object has been freed. |
| [IDirectDrawSurface7::Lock](..\ddraw\nf-ddraw-idirectdrawsurface7-lock.md) | Obtains a pointer to the surface memory. |
| [IDirectDrawSurface7::PageLock](..\ddraw\nf-ddraw-idirectdrawsurface7-pagelock.md) | Prevents a system-memory surface from being paged out while a bit block transfer (bitblt) operation that uses direct memory access (DMA) transfers to or from system memory is in progress. |
| [IDirectDrawSurface7::PageUnlock](..\ddraw\nf-ddraw-idirectdrawsurface7-pageunlock.md) | Unlocks a system-memory surface, which then allows it to be paged out. |
| [IDirectDrawSurface7::ReleaseDC](..\ddraw\nf-ddraw-idirectdrawsurface7-releasedc.md) | Releases the handle of a device context that was previously obtained by using the IDirectDrawSurface7 |
| [IDirectDrawSurface7::Restore](..\ddraw\nf-ddraw-idirectdrawsurface7-restore.md) | Restores a surface that has been lost. This occurs when the surface memory that is associated with the DirectDrawSurface object has been freed. |
| [IDirectDrawSurface7::SetClipper](..\ddraw\nf-ddraw-idirectdrawsurface7-setclipper.md) | Attaches a clipper object to, or deletes one from, this surface. |
| [IDirectDrawSurface7::SetColorKey](..\ddraw\nf-ddraw-idirectdrawsurface7-setcolorkey.md) | Sets the color key value for the DirectDrawSurface object if the hardware supports color keys on a per-surface basis. |
| [IDirectDrawSurface7::SetLOD](..\ddraw\nf-ddraw-idirectdrawsurface7-setlod.md) | Sets the maximum level of detail (LOD) for a managed mipmap surface. This method succeeds only on managed textures. |
| [IDirectDrawSurface7::SetOverlayPosition](..\ddraw\nf-ddraw-idirectdrawsurface7-setoverlayposition.md) | Changes the display coordinates of an overlay surface. |
| [IDirectDrawSurface7::SetPalette](..\ddraw\nf-ddraw-idirectdrawsurface7-setpalette.md) | Attaches a palette object to (or detaches one from) a surface. The surface uses this palette for all subsequent operations. The palette change takes place immediately, without regard to refresh timing. |
| [IDirectDrawSurface7::SetPriority](..\ddraw\nf-ddraw-idirectdrawsurface7-setpriority.md) | Assigns the texture-management priority for this texture. This method succeeds only on managed textures. |
| [IDirectDrawSurface7::SetPrivateData](..\ddraw\nf-ddraw-idirectdrawsurface7-setprivatedata.md) | Associates data with the surface that is intended for use by the application, not by DirectDraw. Data is passed by value, and multiple sets of data can be associated with a single surface. |
| [IDirectDrawSurface7::SetSurfaceDesc](..\ddraw\nf-ddraw-idirectdrawsurface7-setsurfacedesc.md) | Sets the characteristics of an existing surface. |
| [IDirectDrawSurface7::Unlock](..\ddraw\nf-ddraw-idirectdrawsurface7-unlock.md) | Notifies DirectDraw that the direct surface manipulations are complete. |
| [IDirectDrawSurface7::UpdateOverlayDisplay](..\ddraw\nf-ddraw-idirectdrawsurface7-updateoverlaydisplay.md) | The IDirectDrawSurface7 |
| [IDirectDrawSurface7::UpdateOverlayZOrder](..\ddraw\nf-ddraw-idirectdrawsurface7-updateoverlayzorder.md) | Sets the z-order of an overlay. |
| [IDirectDrawSurface7::UpdateOverlay](..\ddraw\nf-ddraw-idirectdrawsurface7-updateoverlay.md) | Repositions or modifies the visual attributes of an overlay surface. These surfaces must have the DDSCAPS_OVERLAY flag set. |
