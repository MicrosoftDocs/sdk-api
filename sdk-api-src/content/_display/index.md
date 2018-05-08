---
UID: TP:display
ms.assetid: 4b099f8f-1e3b-398c-9d48-80f65f6c3468
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Display Devices Reference



Overview of the Display Devices Reference technology.

To develop Display Devices Reference, you need these headers:

 * [cloneviewhelper.h](..\cloneviewhelper\index.md)
 * [ddkernel.h](..\ddkernel\index.md)
 * [ddkmapi.h](..\ddkmapi\index.md)
 * [ddrawi.h](..\ddrawi\index.md)
 * [ddrawint.h](..\ddrawint\index.md)
 * [dmemmgr.h](..\dmemmgr\index.md)
 * [dvp.h](..\dvp\index.md)
 * [dxmini.h](..\dxmini\index.md)

For the programming guide, see [Display Devices Reference](https://review.docs.microsoft.com/en-us/win32-test/display).

## Functions

| Title   | Description   |
| ---- |:---- |
| [DxApi function](..\ddkmapi\nf-ddkmapi-dxapi.md) | The DxApi function accepts commands from the hardware decoder's video capture driver to access the DxApi interface functions that are implemented in a video miniport driver. |
| [HeapVidMemAllocAligned function](..\dmemmgr\nf-dmemmgr-heapvidmemallocaligned.md) | The HeapVidMemAllocAligned function allocates off_screen_memory for a display driver by using the DirectDraw video memory heap manager. |
| [VidMemFree function](..\dmemmgr\nf-dmemmgr-vidmemfree.md) | The VidMemFree function frees off-screen memory allocated for a display driver by HeapVidMemAllocAligned. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [LPDD_NOTIFYCALLBACK callback function](..\ddkmapi\nc-ddkmapi-lpdd_notifycallback.md) | The NotifyCallback callback function performs operations related to an event that occurred. |
| [PDD_CANCREATESURFACE callback function](..\ddrawint\nc-ddrawint-pdd_cancreatesurface.md) | The CanCreateD3DBuffer callback function determines whether the driver can create a driver-level command or vertex buffer of the specified description. |
| [PDD_COLORCB_COLORCONTROL callback function](..\ddrawint\nc-ddrawint-pdd_colorcb_colorcontrol.md) | The DdControlColor callback function controls the luminance and brightness controls of an overlay surface. |
| [PDD_CREATEPALETTE callback function](..\ddrawint\nc-ddrawint-pdd_createpalette.md) | The DdCreatePalette callback function creates a DirectDrawPalette object for the specified DirectDraw object. |
| [PDD_CREATESURFACE callback function](..\ddrawint\nc-ddrawint-pdd_createsurface.md) | The CreateD3DBuffer callback function is used to create a driver-level command or vertex buffer of the specified description. |
| [PDD_CREATESURFACEEX callback function](..\ddrawint\nc-ddrawint-pdd_createsurfaceex.md) | The D3dCreateSurfaceEx function notifies about the association of a Microsoft DirectDraw surface and a Microsoft Direct3D handle value to enable setting up the surface for Direct3D rendering. |
| [PDD_DESTROYDDLOCAL callback function](..\ddrawint\nc-ddrawint-pdd_destroyddlocal.md) | The D3dDestroyDDLocal function destroys all the Microsoft Direct3D surfaces previously created by the D3dCreateSurfaceEx function that belong to the same given local Microsoft DirectDraw object. |
| [PDD_FLIPTOGDISURFACE callback function](..\ddrawint\nc-ddrawint-pdd_fliptogdisurface.md) | The DdFlipToGDISurface callback function notifies the driver when DirectDraw is flipping to or from a GDI surface. |
| [PDD_FREEDRIVERMEMORY callback function](..\ddrawint\nc-ddrawint-pdd_freedrivermemory.md) | The DdFreeDriverMemory callback function frees offscreen or nonlocal display memory to satisfy a new allocation request. |
| [PDD_GETAVAILDRIVERMEMORY callback function](..\ddrawint\nc-ddrawint-pdd_getavaildrivermemory.md) | The DdGetAvailDriverMemory callback function queries the amount of free memory in the driver-managed memory heap. |
| [PDD_GETDRIVERINFO callback function](..\ddrawint\nc-ddrawint-pdd_getdriverinfo.md) | The DdGetDriverInfo function queries the driver for additional DirectDraw and Direct3D functionality that the driver supports. |
| [PDD_GETDRIVERSTATE callback function](..\ddrawint\nc-ddrawint-pdd_getdriverstate.md) | The D3dGetDriverState function is used by both the Microsoft DirectDraw and Microsoft Direct3D runtimes to obtain information from the driver about its current state. |
| [PDD_GETSCANLINE callback function](..\ddrawint\nc-ddrawint-pdd_getscanline.md) | The DdGetScanLine callback function returns the number of the current physical scan line. |
| [PDD_KERNELCB_SYNCSURFACE callback function](..\ddrawint\nc-ddrawint-pdd_kernelcb_syncsurface.md) | The DdSyncSurfaceData callback function sets and modifies surface data before it is passed to the video miniport driver. |
| [PDD_KERNELCB_SYNCVIDEOPORT callback function](..\ddrawint\nc-ddrawint-pdd_kernelcb_syncvideoport.md) | The DdSyncVideoPortData callback function sets and modifies VPE object data before it is passed to the video miniport driver. |
| [PDD_MAPMEMORY callback function](..\ddrawint\nc-ddrawint-pdd_mapmemory.md) | The DdMapMemory callback function maps application-modifiable portions of the frame buffer into the user-mode address space of the specified process, or unmaps memory. |
| [PDD_MOCOMPCB_BEGINFRAME callback function](..\ddrawint\nc-ddrawint-pdd_mocompcb_beginframe.md) | The DdMoCompBeginFrame callback function starts decoding a new frame. |
| [PDD_MOCOMPCB_CREATE callback function](..\ddrawint\nc-ddrawint-pdd_mocompcb_create.md) | The DdMoCompCreate callback function notifies the driver that a software decoder will start using motion compensation with the specified GUID. |
| [PDD_MOCOMPCB_DESTROY callback function](..\ddrawint\nc-ddrawint-pdd_mocompcb_destroy.md) | The DdMoCompDestroy callback function notifies the driver that this motion compensation object will no longer be used. The driver now needs to perform any necessary cleanup. |
| [PDD_MOCOMPCB_ENDFRAME callback function](..\ddrawint\nc-ddrawint-pdd_mocompcb_endframe.md) | The DdMoCompEndFrame callback function completes a decoded frame. |
| [PDD_MOCOMPCB_GETCOMPBUFFINFO callback function](..\ddrawint\nc-ddrawint-pdd_mocompcb_getcompbuffinfo.md) | The DDMoCompGetBuffInfo callback function allows the driver to specify how many interim surfaces are required to support the specified GUID, and the size, location, and format of each of these surfaces. |
| [PDD_MOCOMPCB_GETFORMATS callback function](..\ddrawint\nc-ddrawint-pdd_mocompcb_getformats.md) | The DdMoCompGetFormats callback function indicates the uncompressed formats to which the hardware can decode the data. |
| [PDD_MOCOMPCB_GETGUIDS callback function](..\ddrawint\nc-ddrawint-pdd_mocompcb_getguids.md) | The DdMoCompGetGuids callback function retrieves the number of GUIDs the driver supports. |
| [PDD_MOCOMPCB_GETINTERNALINFO callback function](..\ddrawint\nc-ddrawint-pdd_mocompcb_getinternalinfo.md) | The DdMoCompGetInternalInfo callback function allows the driver to report that it internally allocates display memory to perform motion compensation. |
| [PDD_MOCOMPCB_QUERYSTATUS callback function](..\ddrawint\nc-ddrawint-pdd_mocompcb_querystatus.md) | The DdMoCompQueryStatus callback function queries the status of the most recent rendering operation to the specified surface. |
| [PDD_MOCOMPCB_RENDER callback function](..\ddrawint\nc-ddrawint-pdd_mocompcb_render.md) | The DdMoCompRender callback function tells the driver what macroblocks to render by specifying the surfaces containing the macroblocks, the offsets in each surface where the macroblocks exist, and the size of the macroblock data to be rendered. |
| [PDD_PALCB_DESTROYPALETTE callback function](..\ddrawint\nc-ddrawint-pdd_palcb_destroypalette.md) | The DdDestroyPalette callback function destroys the specified palette. |
| [PDD_PALCB_SETENTRIES callback function](..\ddrawint\nc-ddrawint-pdd_palcb_setentries.md) | The DdSetEntries callback function updates the palette entries in the specified palette. |
| [PDD_SETEXCLUSIVEMODE callback function](..\ddrawint\nc-ddrawint-pdd_setexclusivemode.md) | The DdSetExclusiveMode callback function notifies the driver when a DirectDraw application is switching to or from exclusive mode. |
| [PDD_SURFCB_ADDATTACHEDSURFACE callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_addattachedsurface.md) | The DdAddAttachedSurface callback function attaches a surface to another surface. |
| [PDD_SURFCB_BLT callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_blt.md) | The DdBlt callback function performs a bit-block transfer. |
| [PDD_SURFCB_DESTROYSURFACE callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_destroysurface.md) | The DdDestroySurface callback function destroys a DirectDraw surface. |
| [PDD_SURFCB_FLIP callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_flip.md) | The DdFlip callback function causes the surface memory associated with the target surface to become the primary surface, and the current surface to become the nonprimary surface. |
| [PDD_SURFCB_GETBLTSTATUS callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_getbltstatus.md) | The DdGetBltStatus callback function queries the blit status of the specified surface. |
| [PDD_SURFCB_GETFLIPSTATUS callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_getflipstatus.md) | The DdGetFlipStatus callback function determines whether the most recently requested flip on a surface has occurred. |
| [PDD_SURFCB_LOCK callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_lock.md) | The DdLock callback function locks a specified area of surface memory and provides a valid pointer to a block of memory associated with a surface. |
| [PDD_SURFCB_SETCOLORKEY callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_setcolorkey.md) | The DdSetColorKey callback function sets the color key value for the specified surface. |
| [PDD_SURFCB_SETOVERLAYPOSITION callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_setoverlayposition.md) | The DdSetOverlayPosition callback function sets the position for an overlay. |
| [PDD_SURFCB_SETPALETTE callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_setpalette.md) | The DdSetPalette callback function attaches a palette to the specified surface. |
| [PDD_SURFCB_UNLOCK callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_unlock.md) | The DdUnLock callback function releases the lock held on the specified surface. |
| [PDD_SURFCB_UPDATEOVERLAY callback function](..\ddrawint\nc-ddrawint-pdd_surfcb_updateoverlay.md) | The DdUpdateOverlay callback function repositions or modifies the visual attributes of an overlay surface. |
| [PDD_VPORTCB_CANCREATEVIDEOPORT callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_cancreatevideoport.md) | The DdVideoPortCanCreate callback function determines whether the driver can support a DirectDraw VPE object of the specified description. |
| [PDD_VPORTCB_COLORCONTROL callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_colorcontrol.md) | The DdVideoPortColorControl callback function gets or sets the VPE object color controls. |
| [PDD_VPORTCB_CREATEVIDEOPORT callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_createvideoport.md) | The DdVideoPortCreate callback function notifies the driver that DirectDraw has created a VPE object. |
| [PDD_VPORTCB_DESTROYVPORT callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_destroyvport.md) | The DdVideoPortDestroy callback function notifies the driver that DirectDraw has destroyed the specified VPE object. |
| [PDD_VPORTCB_FLIP callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_flip.md) | The DdVideoPortFlip callback function performs a physical flip, causing the VPE object to start writing data to the new surface. |
| [PDD_VPORTCB_GETBANDWIDTH callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_getbandwidth.md) | The DdVideoPortGetBandwidth callback function reports the bandwidth limitations of the device's frame buffer memory based the specified VPE object output format. |
| [PDD_VPORTCB_GETFIELD callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_getfield.md) | The DdVideoPortGetField callback function determines whether the current field of an interlaced signal is even or odd. |
| [PDD_VPORTCB_GETFLIPSTATUS callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_getflipstatus.md) | The DdVideoPortGetFlipStatus callback function determines whether the most recently requested flip on a surface has occurred. |
| [PDD_VPORTCB_GETINPUTFORMATS callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_getinputformats.md) | The DdVideoPortGetInputFormats callback function determines the input formats that the DirectDraw VPE object can accept. |
| [PDD_VPORTCB_GETLINE callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_getline.md) | The DdVideoPortGetLine callback function returns the current line number of the hardware video port. |
| [PDD_VPORTCB_GETOUTPUTFORMATS callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_getoutputformats.md) | The DdVideoPortGetOutputFormats callback function determines the output formats that the VPE object supports. |
| [PDD_VPORTCB_GETSIGNALSTATUS callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_getsignalstatus.md) | The DdVideoPortGetSignalStatus callback function retrieves the status of the video signal currently being presented to the hardware video port. |
| [PDD_VPORTCB_GETVPORTCONNECT callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_getvportconnect.md) | The DdVideoPortGetConnectInfo callback function returns the connections supported by the specified VPE object. |
| [PDD_VPORTCB_UPDATE callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_update.md) | The DdVideoPortUpdate callback function starts and stops the VPE object, and modifies the VPE object data stream. |
| [PDD_VPORTCB_WAITFORSYNC callback function](..\ddrawint\nc-ddrawint-pdd_vportcb_waitforsync.md) | The DdVideoPortWaitForSync callback function waits until the next vertical synch occurs. |
| [PDD_WAITFORVERTICALBLANK callback function](..\ddrawint\nc-ddrawint-pdd_waitforverticalblank.md) | The DdWaitForVerticalBlank callback function returns the vertical blank status of the device. |
| [PDX_BOBNEXTFIELD callback function](..\dxmini\nc-dxmini-pdx_bobnextfield.md) | The DxBobNextField callback function bobs the next field of interleaved data. |
| [PDX_ENABLEIRQ callback function](..\dxmini\nc-dxmini-pdx_enableirq.md) | The DxEnableIRQ callback function indicates to the video miniport driver which IRQs should be enabled or disabled. |
| [PDX_FLIPOVERLAY callback function](..\dxmini\nc-dxmini-pdx_flipoverlay.md) | The DxFlipOverlay callback function is called when a client of the video miniport driver wants to flip the overlay or when autoflipping is enabled. |
| [PDX_FLIPVIDEOPORT callback function](..\dxmini\nc-dxmini-pdx_flipvideoport.md) | The DxFlipVideoPort callback function is called when a client of the video miniport driver wants to flip the video port extensions (VPE) object or when autoflipping is enabled. |
| [PDX_GETCURRENTAUTOFLIP callback function](..\dxmini\nc-dxmini-pdx_getcurrentautoflip.md) | The DxGetCurrentAutoflip callback function is called when the device is hardware autoflipping and a client of the video miniport driver wants to know which surface is receiving the current field of video data for capture purposes. |
| [PDX_GETIRQINFO callback function](..\dxmini\nc-dxmini-pdx_getirqinfo.md) | The DxGetIRQInfo callback function indicates that the driver manages the interrupt request. |
| [PDX_GETPOLARITY callback function](..\dxmini\nc-dxmini-pdx_getpolarity.md) | The DxGetPolarity callback function returns the polarity (even or odd) of the current field being written by the video port extensions (VPE) object. |
| [PDX_GETPREVIOUSAUTOFLIP callback function](..\dxmini\nc-dxmini-pdx_getpreviousautoflip.md) | The DxGetPreviousAutoflip callback function is called when the device is hardware autoflipping and a client of the video miniport driver wants to know which surface received the previous field of video data for capture purposes. |
| [PDX_GETTRANSFERSTATUS callback function](..\dxmini\nc-dxmini-pdx_gettransferstatus.md) | The DxGetTransferStatus callback function is used by DirectDraw to determine which hardware bus master has completed. |
| [PDX_IRQCALLBACK callback function](..\dxmini\nc-dxmini-pdx_irqcallback.md) | The IRQCallback function performs operations related to the IRQ that occurred. |
| [PDX_LOCK callback function](..\dxmini\nc-dxmini-pdx_lock.md) | The DxLock callback function is called when a client of the video miniport driver wants access to the frame buffer. |
| [PDX_SETSTATE callback function](..\dxmini\nc-dxmini-pdx_setstate.md) | The DxSetState callback function is called when a client of the video miniport driver decides it wants to switch from bob mode to weave mode, and vice versa. |
| [PDX_SKIPNEXTFIELD callback function](..\dxmini\nc-dxmini-pdx_skipnextfield.md) | The DxSkipNextField callback function is called when the next field needs to be skipped or reenabled. |
| [PDX_TRANSFER callback function](..\dxmini\nc-dxmini-pdx_transfer.md) | The DxTransfer callback function informs the driver to bus master data from a surface to the buffer specified in the memory descriptor list (MDL). |

## Structures

| Title   | Description   |
| ---- |:---- |
| [DDVIDEOPORTDATA structure](..\dxmini\ns-dxmini-ddvideoportdata.md) | The DDVIDEOPORTDATA structure is used by DirectDraw to represent a video port extensions (VPE) object to the kernel-mode video miniport driver. |
| [DD_CALLBACKS structure](..\ddrawint\ns-ddrawint-dd_callbacks.md) | The DD_CALLBACKS structure contains entry pointers to the callback functions that a device driver supports. |
| [DD_KERNELCALLBACKS structure](..\ddrawint\ns-ddrawint-dd_kernelcallbacks.md) | The DD_KERNELCALLBACKS structure contains entry pointers to the DirectDraw kernel-mode callback functions that the driver supports. |
| [DD_MOTIONCOMPCALLBACKS structure](..\ddrawint\ns-ddrawint-dd_motioncompcallbacks.md) | The DD_MOTIONCOMPCALLBACKS structure contains entry pointers to the motion compensation callback functions that a device driver supports. |
| [DD_NTPRIVATEDRIVERCAPS structure](..\ddrawint\ns-ddrawint-dd_ntprivatedrivercaps.md) | The DD_NTPRIVATEDRIVERCAPS structure enables the driver to change the behavior of Microsoft DirectDraw when DirectDraw is creating surfaces. |
| [DD_PALETTECALLBACKS structure](..\ddrawint\ns-ddrawint-dd_palettecallbacks.md) | The DD_PALETTECALLBACKS structure contains entry pointers to the DirectDraw palette callback functions that a device driver supports. |
| [DD_SURFACECALLBACKS structure](..\ddrawint\ns-ddrawint-dd_surfacecallbacks.md) | The DD_SURFACECALLBACKS structure contains entry pointers to the Microsoft DirectDraw surface callback functions that a device driver supports. |
| [DD_VIDEOPORTCALLBACKS structure](..\ddrawint\ns-ddrawint-dd_videoportcallbacks.md) | The DD_VIDEOPORTCALLBACKS structure contains entry pointers to Microsoft DirectDraw video port extensions (VPE) callback functions that a device driver supports. |
| [_DDADDVPCAPTUREBUFF structure](..\ddkmapi\ns-ddkmapi-_ddaddvpcapturebuff.md) | The DDADDVPCAPTUREBUFF structure contains the information required to add a new buffer to the internal capture queue. |
| [_DDBOBNEXTFIELDINFO structure](..\dxmini\ns-dxmini-_ddbobnextfieldinfo.md) | The DDBOBNEXTFIELDINFO structure contains the bob information for the surface. |
| [_DDCAPBUFFINFO structure](..\ddkmapi\ns-ddkmapi-_ddcapbuffinfo.md) | The DDCAPBUFFINFO structure contains the capture information. |
| [_DDCLOSEHANDLE structure](..\ddkmapi\ns-ddkmapi-_ddclosehandle.md) | The DDCLOSEHANDLE structure contains the Microsoft DirectDraw object, surface, video port extensions (VPE) object, or VPE capture handle. |
| [_DDCOMPBUFFERINFO structure](..\ddrawint\ns-ddrawint-_ddcompbufferinfo.md) | The DDCOMPBUFFERINFO structure contains driver-supplied information regarding compression buffers. |
| [_DDCORECAPS structure](..\ddrawi\ns-ddrawi-_ddcorecaps.md) | The DDCORECAPS structure specifies the core capabilities of the Microsoft DirectDraw driver and its device, which are exposed to an application through the DirectDraw object. |
| [_DDENABLEIRQINFO structure](..\dxmini\ns-dxmini-_ddenableirqinfo.md) | The DDENABLEIRQINFO structure contains the information required to enable interrupts. |
| [_DDFLIPOVERLAY structure](..\ddkmapi\ns-ddkmapi-_ddflipoverlay.md) | The DDFLIPOVERLAY structure contains the surface information required for the flip. |
| [_DDFLIPOVERLAYINFO structure](..\dxmini\ns-dxmini-_ddflipoverlayinfo.md) | The DDFLIPOVERLAYINFO structure contains the flip information for the surface. |
| [_DDFLIPVIDEOPORT structure](..\ddkmapi\ns-ddkmapi-_ddflipvideoport.md) | The DDFLIPVIDEOPORT structure contains the information required to flip the hardware video port. |
| [_DDFLIPVIDEOPORTINFO structure](..\dxmini\ns-dxmini-_ddflipvideoportinfo.md) | The DDFLIPVIDEOPORTINFO structure contains the video port extensions (VPE) object and surface information. |
| [_DDGETAUTOFLIPIN structure](..\ddkmapi\ns-ddkmapi-_ddgetautoflipin.md) | The DDGETAUTOFLIPIN structure contains the handle information. |
| [_DDGETAUTOFLIPOUT structure](..\ddkmapi\ns-ddkmapi-_ddgetautoflipout.md) | The DDGETAUTOFLIPOUT structure contains the handle and polarity information returned from the DD_DXAPI_GET_CURRENT_VP_AUTOFLIP_SURFACE and DD_DXAPI_GET_LAST_VP_AUTOFLIP_SURFACE function identifiers of the DxApi function. |
| [_DDGETCURRENTAUTOFLIPININFO structure](..\dxmini\ns-dxmini-_ddgetcurrentautoflipininfo.md) | The DDGETCURRENTAUTOFLIPININFO structure contains the video port extensions (VPE) object information. |
| [_DDGETCURRENTAUTOFLIPOUTINFO structure](..\dxmini\ns-dxmini-_ddgetcurrentautoflipoutinfo.md) | The DDGETCURRENTAUTOFLIPOUTINFO structure provides the surface information. |
| [_DDGETFIELDNUMIN structure](..\ddkmapi\ns-ddkmapi-_ddgetfieldnumin.md) | The DDGETFIELDNUMIN structure contains the Microsoft DirectDraw and video port extensions (VPE) object handle information. |
| [_DDGETFIELDNUMOUT structure](..\ddkmapi\ns-ddkmapi-_ddgetfieldnumout.md) | The DDGETFIELDNUMOUT structure contains the hardware video port's field number. |
| [_DDGETIRQINFO structure](..\dxmini\ns-dxmini-_ddgetirqinfo.md) | The DDGETIRQINFO structure contains interrupt information for the video miniport driver. |
| [_DDGETKERNELCAPSOUT structure](..\ddkmapi\ns-ddkmapi-_ddgetkernelcapsout.md) | The DDGETKERNELCAPSOUT structure contains the capabilities of the Microsoft DirectDraw object. |
| [_DDGETPOLARITYIN structure](..\ddkmapi\ns-ddkmapi-_ddgetpolarityin.md) | The DDGETPOLARITYIN structure contains the Microsoft DirectDraw and video port extensions (VPE) object handles. |
| [_DDGETPOLARITYININFO structure](..\dxmini\ns-dxmini-_ddgetpolarityininfo.md) | The DDGETPOLARITYININFO structure contains the video port extensions (VPE) object information. |
| [_DDGETPOLARITYOUT structure](..\ddkmapi\ns-ddkmapi-_ddgetpolarityout.md) | The DDGETPOLARITYOUT structure contains the requested polarity information. |
| [_DDGETPOLARITYOUTINFO structure](..\dxmini\ns-dxmini-_ddgetpolarityoutinfo.md) | The DDGETPOLARITYOUTINFO structure contains the polarity information of the video port extensions (VPE) object. |
| [_DDGETPREVIOUSAUTOFLIPININFO structure](..\dxmini\ns-dxmini-_ddgetpreviousautoflipininfo.md) | The DDGETPREVIOUSAUTOFLIPININFO structure provides the video port extensions (VPE) object information. |
| [_DDGETPREVIOUSAUTOFLIPOUTINFO structure](..\dxmini\ns-dxmini-_ddgetpreviousautoflipoutinfo.md) | The DDGETPREVIOUSAUTOFLIPOUTINFO structure provides the surface data. |
| [_DDGETSURFACESTATEIN structure](..\ddkmapi\ns-ddkmapi-_ddgetsurfacestatein.md) | The DDGETSURFACESTATEIN structure contains the Microsoft DirectDraw and DirectDraw surface handle information. |
| [_DDGETSURFACESTATEOUT structure](..\ddkmapi\ns-ddkmapi-_ddgetsurfacestateout.md) | The DDGETSURFACESTATEOUT structure contains the capabilities and status of the specified surface. |
| [_DDGETTRANSFERSTATUSOUTINFO structure](..\dxmini\ns-dxmini-_ddgettransferstatusoutinfo.md) | The DDGETTRANSFERSTATUSOUTINFO structure contains the transfer status information. |
| [_DDGETVERSIONNUMBER structure](..\ddkmapi\ns-ddkmapi-_ddgetversionnumber.md) | The DDGETVERSIONNUMBER structure contains the version number of the kernel-mode video transport component of Microsoft DirectDraw that is supported by the video miniport driver's DxApi interface. |
| [_DDHAL_DESTROYDDLOCALDATA structure](..\ddrawi\ns-ddrawi-_ddhal_destroyddlocaldata.md) | DDHAL_DESTROYDDLOCALDATA contains the information required for the driver to destroy a set of surfaces associated to a given local DirectDraw object. |
| [_DDKERNELCAPS structure](..\ddkernel\ns-ddkernel-_ddkernelcaps.md) | The DDKERNELCAPS structure notifies the client what support, if any, exists in the miniport driver for the kernel-mode video transport. |
| [_DDLOCKIN structure](..\ddkmapi\ns-ddkmapi-_ddlockin.md) | The DDLOCKIN structure contains the Microsoft DirectDraw object and DirectDraw surface handle information. |
| [_DDLOCKININFO structure](..\dxmini\ns-dxmini-_ddlockininfo.md) | The DDLOCKININFO structure contains the surface information. |
| [_DDLOCKOUT structure](..\ddkmapi\ns-ddkmapi-_ddlockout.md) | The DDLOCKOUT structure contains a description of the surface. |
| [_DDLOCKOUTINFO structure](..\dxmini\ns-dxmini-_ddlockoutinfo.md) | The DDLOCKOUTINFO structure contains the surface information output from the DxLock function. |
| [_DDMOCOMPBUFFERINFO structure](..\ddrawint\ns-ddrawint-_ddmocompbufferinfo.md) | The DDMOCOMPBUFFERINFO structure contains the macro block information required to render a frame and passes this information to the DD_RENDERMOCOMPDATA structure. |
| [_DDOPENDIRECTDRAWIN structure](..\ddkmapi\ns-ddkmapi-_ddopendirectdrawin.md) | The DDOPENDIRECTDRAWIN structure contains the Microsoft DirectDraw object information. |
| [_DDOPENDIRECTDRAWOUT structure](..\ddkmapi\ns-ddkmapi-_ddopendirectdrawout.md) | The DDOPENDIRECTDRAWOUT structure contains a new Microsoft DirectDraw handle for the DD_DXAPI_OPENDIRECTDRAW function identifier of the DxApi function if the ddRVal member of DDOPENDIRECTDRAWOUT is set to DD_OK. |
| [_DDOPENSURFACEIN structure](..\ddkmapi\ns-ddkmapi-_ddopensurfacein.md) | The DDOPENSURFACEIN structure contains the DirectDrawSurface object information. |
| [_DDOPENSURFACEOUT structure](..\ddkmapi\ns-ddkmapi-_ddopensurfaceout.md) | The DDOPENSURFACEOUT structure contains a new DirectDrawSurface handle, if the ddRVal member of DDOPENSURFACEOUT is set to DD_OK. This new handle must be used on all subsequent calls that require a DirectDrawSurface handle. |
| [_DDOPENVIDEOPORTIN structure](..\ddkmapi\ns-ddkmapi-_ddopenvideoportin.md) | The DDOPENVIDEOPORTIN structure contains the video port extensions (VPE) object information. |
| [_DDOPENVIDEOPORTOUT structure](..\ddkmapi\ns-ddkmapi-_ddopenvideoportout.md) | The DDOPENVIDEOPORTOUT structure contains a Microsoft DirectDraw return code and a new surface handle if ddRVal is set to DD_OK. This new handle must be used on all subsequent calls that require a video port extensions (VPE) object handle. |
| [_DDOPENVPCAPTUREDEVICEIN structure](..\ddkmapi\ns-ddkmapi-_ddopenvpcapturedevicein.md) | The DDOPENVPCAPTUREDEVICEIN structure contains the video port extensions (VPE) capture information. |
| [_DDOPENVPCAPTUREDEVICEOUT structure](..\ddkmapi\ns-ddkmapi-_ddopenvpcapturedeviceout.md) | The DDOPENVPCAPTUREDEVICEOUT structure contains the video port extensions (VPE) capture handle. |
| [_DDREGISTERCALLBACK structure](..\ddkmapi\ns-ddkmapi-_ddregistercallback.md) | The DDREGISTERCALLBACK structure contains the register callback information. This structure is used by both the DD_DXAPI_REGISTER_CALLBACK and DD_DXAPI_UNREGISTER_CALLBACK function identifiers of the DxApi function. |
| [_DDSETFIELDNUM structure](..\ddkmapi\ns-ddkmapi-_ddsetfieldnum.md) | The DDSETFIELDNUM structure contains the handles and the field number. |
| [_DDSETSKIPFIELD structure](..\ddkmapi\ns-ddkmapi-_ddsetskipfield.md) | The DDSETSKIPFIELD structure contains the start field information. |
| [_DDSETSTATEININFO structure](..\dxmini\ns-dxmini-_ddsetstateininfo.md) | The DDSETSTATEININFO structure contains the surface and video port extensions (VPE) object information. |
| [_DDSETSTATEOUTINFO structure](..\dxmini\ns-dxmini-_ddsetstateoutinfo.md) | The DDSETSTATEOUTINFO structure contains the state information for the video port extensions (VPE) object. |
| [_DDSETSURFACETATE structure](..\ddkmapi\ns-ddkmapi-_ddsetsurfacetate.md) | The DDSETSURFACESTATE structure contains the surface state information. |
| [_DDSKIPNEXTFIELDINFO structure](..\dxmini\ns-dxmini-_ddskipnextfieldinfo.md) | The DDSKIPNEXTFIELDINFO structure contains the skip information for the video port extensions (VPE) object. |
| [_DDSURFACEDATA structure](..\dxmini\ns-dxmini-_ddsurfacedata.md) | The DDSURFACEDATA structure is used by DirectDraw to represent a surface to the kernel-mode miniport driver. |
| [_DDTRANSFERININFO structure](..\dxmini\ns-dxmini-_ddtransferininfo.md) | The DDTRANSFERININFO structure contains the transfer information for the surface |
| [_DDTRANSFEROUTINFO structure](..\dxmini\ns-dxmini-_ddtransferoutinfo.md) | The DDTRANSFEROUTINFO structure returns the polarity of the field being captured. |
| [_DDVIDEOPORTBANDWIDTH structure](..\dvp\ns-dvp-_ddvideoportbandwidth.md) | The DDVIDEOPORTBANDWIDTH structure describes the bandwidth characteristics of an overlay when used with a particular video port extensions (VPE) object/pixel format configuration. |
| [_DDVIDEOPORTCAPS structure](..\dvp\ns-dvp-_ddvideoportcaps.md) | The DDVIDEOPORTCAPS structure describes the capabilities and alignment restrictions of a hardware video port. |
| [_DDVIDEOPORTCONNECT structure](..\dvp\ns-dvp-_ddvideoportconnect.md) | The DDVIDEOPORTCONNECT structure describes a hardware video port connection. |
| [_DDVIDEOPORTDESC structure](..\dvp\ns-dvp-_ddvideoportdesc.md) | The DDVIDEOPORTDESC structure describes the video port extensions (VPE) object being created. |
| [_DDVIDEOPORTINFO structure](..\dvp\ns-dvp-_ddvideoportinfo.md) | The DDVIDEOPORTINFO structure describes how the driver should transfer video data to a surface (or to surfaces); DDVIDEOPORTINFO is a member of the DD_VIDEOPORT_LOCAL structure. |
| [_DD_ADDATTACHEDSURFACEDATA structure](..\ddrawint\ns-ddrawint-_dd_addattachedsurfacedata.md) | The DD_ADDATTACHEDSURFACEDATA structure contains information necessary to attach a surface to another surface. |
| [_DD_ATTACHLIST structure](..\ddrawint\ns-ddrawint-_dd_attachlist.md) | The DD_ATTACHLIST structure maintains a list of attached surfaces for Microsoft DirectDraw. |
| [_DD_BEGINMOCOMPFRAMEDATA structure](..\ddrawint\ns-ddrawint-_dd_beginmocompframedata.md) | The DDHAL_BEGINMOCOMPFRAMEDATA structure contains the frame information required to start decoding. |
| [_DD_BLTDATA structure](..\ddrawint\ns-ddrawint-_dd_bltdata.md) | The DD_BLTDATA structure contains the information relevant to the driver for doing bit block transfers. |
| [_DD_CANCREATESURFACEDATA structure](..\ddrawint\ns-ddrawint-_dd_cancreatesurfacedata.md) | The DD_CANCREATESURFACEDATA structure contains information necessary to indicate whether a surface--in the case of CanCreateD3DBuffer, a buffer--can be created. |
| [_DD_CANCREATEVPORTDATA structure](..\ddrawint\ns-ddrawint-_dd_cancreatevportdata.md) | The DD_CANCREATEVPORTDATA structure contains the information required for the driver to determine whether a video port extensions (VPE) object can be created. |
| [_DD_CLIPPER_GLOBAL structure](..\ddrawint\ns-ddrawint-_dd_clipper_global.md) | The DD_CLIPPER_GLOBAL structure contains the global DirectDrawClipper data that can be shared between object instances. |
| [_DD_CLIPPER_LOCAL structure](..\ddrawint\ns-ddrawint-_dd_clipper_local.md) | The DD_CLIPPER_LOCAL structure contains local data for each individual DirectDrawClipper object. |
| [_DD_COLORCONTROLCALLBACKS structure](..\ddrawint\ns-ddrawint-_dd_colorcontrolcallbacks.md) | The DD_COLORCONTROLCALLBACKS structure contains an entry pointer to the Microsoft DirectDraw color control callback that a device driver supports. |
| [_DD_COLORCONTROLDATA structure](..\ddrawint\ns-ddrawint-_dd_colorcontroldata.md) | The DD_COLORCONTROLDATA structure contains the color control information for the specified overlay. |
| [_DD_CREATEMOCOMPDATA structure](..\ddrawint\ns-ddrawint-_dd_createmocompdata.md) | The DD_CREATEMOCOMPDATA structure contains the data required to begin using motion compensation. |
| [_DD_CREATEPALETTEDATA structure](..\ddrawint\ns-ddrawint-_dd_createpalettedata.md) | The DD_CREATEPALETTEDATA structure contains information necessary to create a DirectDrawPalette object for this Microsoft DirectDraw object. |
| [_DD_CREATESURFACEDATA structure](..\ddrawint\ns-ddrawint-_dd_createsurfacedata.md) | The DD_CREATESURFACEDATA structure contains information necessary to create a surface--in the case of CreateD3DBuffer, a command or vertex buffer. |
| [_DD_CREATESURFACEEXDATA structure](..\ddrawint\ns-ddrawint-_dd_createsurfaceexdata.md) | The DD_CREATESURFACEEXDATA structure contains information required for the driver to create a surface and associate with it a supplied texture handle. |
| [_DD_CREATEVPORTDATA structure](..\ddrawint\ns-ddrawint-_dd_createvportdata.md) | The DD_CREATEVPORTDATA structure contains the information necessary to describe the video port extensions (VPE) object being created. |
| [_DD_D3DBUFCALLBACKS structure](..\ddrawint\ns-ddrawint-_dd_d3dbufcallbacks.md) | The DD_D3DBUFCALLBACKS structure is used only by drivers that implement driver level allocation of command and vertex buffers. |
| [_DD_DESTROYMOCOMPDATA structure](..\ddrawint\ns-ddrawint-_dd_destroymocompdata.md) | The DD_DESTROYMOCOMPDATA structure contains the information required to finish performing motion compensation. |
| [_DD_DESTROYPALETTEDATA structure](..\ddrawint\ns-ddrawint-_dd_destroypalettedata.md) | The DD_DESTROYPALETTEDATA structure contains information necessary to destroy the specified palette. |
| [_DD_DESTROYSURFACEDATA structure](..\ddrawint\ns-ddrawint-_dd_destroysurfacedata.md) | The DD_DESTROYSURFACEDATA structure contains information necessary to destroy the specified surface--in the case of DestroyD3DBuffer, a command or vertex buffer. |
| [_DD_DESTROYVPORTDATA structure](..\ddrawint\ns-ddrawint-_dd_destroyvportdata.md) | The DD_DESTROYVPORTDATA structure contains the information necessary for the driver to clean up. |
| [_DD_DIRECTDRAW_GLOBAL structure](..\ddrawint\ns-ddrawint-_dd_directdraw_global.md) | The DD_DIRECTDRAW_GLOBAL structure contains driver information that describes the driver's device. |
| [_DD_DIRECTDRAW_LOCAL structure](..\ddrawint\ns-ddrawint-_dd_directdraw_local.md) | The DD_DIRECTDRAW_LOCAL structure contains driver information that is relevant to the current DirectDraw process only. |
| [_DD_ENDMOCOMPFRAMEDATA structure](..\ddrawint\ns-ddrawint-_dd_endmocompframedata.md) | The DD_ENDMOCOMPFRAMEDATA structure contains information required to complete a decoded frame. |
| [_DD_FLIPDATA structure](..\ddrawint\ns-ddrawint-_dd_flipdata.md) | The DD_FLIPDATA structure contains information needed to do a flip. |
| [_DD_FLIPTOGDISURFACEDATA structure](..\ddrawint\ns-ddrawint-_dd_fliptogdisurfacedata.md) | The DD_FLIPTOGDISURFACEDATA structure contains the GDI surface notification information. |
| [_DD_FLIPVPORTDATA structure](..\ddrawint\ns-ddrawint-_dd_flipvportdata.md) | The DD_FLIPVPORTDATA structure contains the information necessary for the video port extensions (VPE) object to perform a flip. |
| [_DD_FREEDRIVERMEMORYDATA structure](..\ddrawint\ns-ddrawint-_dd_freedrivermemorydata.md) | The DD_FREEDRIVERMEMORYDATA structure contains the details of the free request. |
| [_DD_GETAVAILDRIVERMEMORYDATA structure](..\ddrawint\ns-ddrawint-_dd_getavaildrivermemorydata.md) | The DD_GETAVAILDRIVERMEMORYDATA structure contains the information needed by the driver to query and return the amount of free memory. |
| [_DD_GETBLTSTATUSDATA structure](..\ddrawint\ns-ddrawint-_dd_getbltstatusdata.md) | The DD_GETBLTSTATUSDATA structure returns the blit status information. |
| [_DD_GETDRIVERINFODATA structure](..\ddrawint\ns-ddrawint-_dd_getdriverinfodata.md) | The DD_GETDRIVERINFODATA structure is used to pass data to and from the DdGetDriverInfo callback routine. |
| [_DD_GETDRIVERSTATEDATA structure](..\ddrawint\ns-ddrawint-_dd_getdriverstatedata.md) | The DD_GETDRIVERSTATEDATA structure describes the state of the driver. |
| [_DD_GETFLIPSTATUSDATA structure](..\ddrawint\ns-ddrawint-_dd_getflipstatusdata.md) | The DD_GETFLIPSTATUSDATA structure returns the flip status information. |
| [_DD_GETHEAPALIGNMENTDATA structure](..\dmemmgr\ns-dmemmgr-_dd_getheapalignmentdata.md) | The DD_GETHEAPALIGNMENTDATA structure contains data on required alignments from a particular heap. |
| [_DD_GETINTERNALMOCOMPDATA structure](..\ddrawint\ns-ddrawint-_dd_getinternalmocompdata.md) | The DD_GETINTERNALMOCOMPDATA structure contains the internal memory requirements. |
| [_DD_GETMOCOMPCOMPBUFFDATA structure](..\ddrawint\ns-ddrawint-_dd_getmocompcompbuffdata.md) | The DD_GETMOCOMPCOMPBUFFDATA structure contains the compressed buffer information. |
| [_DD_GETMOCOMPFORMATSDATA structure](..\ddrawint\ns-ddrawint-_dd_getmocompformatsdata.md) | The DD_GETMOCOMPFORMATSDATA structure contains the uncompressed format information. |
| [_DD_GETMOCOMPGUIDSDATA structure](..\ddrawint\ns-ddrawint-_dd_getmocompguidsdata.md) | The DD_GETMOCOMPGUIDSDATA structure contains the motion compensation GUID information. |
| [_DD_GETSCANLINEDATA structure](..\ddrawint\ns-ddrawint-_dd_getscanlinedata.md) | The DD_GETSCANLINEDATA structure contains the members required to query and return the number of the current scan line. |
| [_DD_GETVPORTBANDWIDTHDATA structure](..\ddrawint\ns-ddrawint-_dd_getvportbandwidthdata.md) | The DD_GETVPORTBANDWIDTHDATA structure contains the bandwidth information for any specified format. |
| [_DD_GETVPORTCONNECTDATA structure](..\ddrawint\ns-ddrawint-_dd_getvportconnectdata.md) | The DD_GETVPORTCONNECTDATA structure contains the connection combinations supported by the specified video port extensions (VPE) object. |
| [_DD_GETVPORTFIELDDATA structure](..\ddrawint\ns-ddrawint-_dd_getvportfielddata.md) | The DD_GETVPORTFIELDDATA structure contains the information required for the driver to determine whether the current field of an interlaced signal is even or odd. |
| [_DD_GETVPORTFLIPSTATUSDATA structure](..\ddrawint\ns-ddrawint-_dd_getvportflipstatusdata.md) | The DD_GETVPORTFLIPSTATUSDATA structure contains the flip status information for the specified surface. |
| [_DD_GETVPORTINPUTFORMATDATA structure](..\ddrawint\ns-ddrawint-_dd_getvportinputformatdata.md) | The DD_GETVPORTINPUTFORMATDATA structure contains the information required for the driver to return the input formats that the video port extensions (VPE) object can accept. |
| [_DD_GETVPORTLINEDATA structure](..\ddrawint\ns-ddrawint-_dd_getvportlinedata.md) | The DD_GETVPORTLINEDATA structure contains the current line number of the hardware video port. |
| [_DD_GETVPORTOUTPUTFORMATDATA structure](..\ddrawint\ns-ddrawint-_dd_getvportoutputformatdata.md) | The DD_GETVPORTOUTPUTFORMATDATA structure contains the information required for the driver to return all of the output formats that the video port extensions (VPE) object supports for a given input format. |
| [_DD_GETVPORTSIGNALDATA structure](..\ddrawint\ns-ddrawint-_dd_getvportsignaldata.md) | The DD_GETVPORTSIGNALDATA structure contains the signal status of the hardware video port. |
| [_DD_HALINFO structure](..\ddrawint\ns-ddrawint-_dd_halinfo.md) | The DD_HALINFO structure describes the capabilities of the hardware and driver. |
| [_DD_LOCKDATA structure](..\ddrawint\ns-ddrawint-_dd_lockdata.md) | The DD_LOCKDATA structure contains information necessary to do a lock as defined by the Microsoft DirectDraw parameter structures. |
| [_DD_MAPMEMORYDATA structure](..\ddrawint\ns-ddrawint-_dd_mapmemorydata.md) | The DD_MAPMEMORYDATA structure contains the information necessary to map or unmap a frame buffer into user-mode memory. |
| [_DD_MISCELLANEOUS2CALLBACKS structure](..\ddrawint\ns-ddrawint-_dd_miscellaneous2callbacks.md) | The DD_MISCELLANEOUS2CALLBACKS structure is used to return the addresses of miscellaneous callback routines. |
| [_DD_MISCELLANEOUSCALLBACKS structure](..\ddrawint\ns-ddrawint-_dd_miscellaneouscallbacks.md) | The DD_MISCELLANEOUSCALLBACKS structure contains an entry pointer to the memory query callback that a device driver supports. |
| [_DD_MORESURFACECAPS structure](..\ddrawint\ns-ddrawint-_dd_moresurfacecaps.md) | The DD_MORESURFACECAPS structure defines more driver surface capabilities in addition to those described in DDCORECAPS. |
| [_DD_MOTIONCOMP_LOCAL structure](..\ddrawint\ns-ddrawint-_dd_motioncomp_local.md) | The DD_MOTIONCOMP_LOCAL structure contains local data for each individual Microsoft DirectDraw motion compensation object. |
| [_DD_NONLOCALVIDMEMCAPS structure](..\ddrawint\ns-ddrawint-_dd_nonlocalvidmemcaps.md) | The DD_NONLOCALVIDMEMCAPS structure contains the capabilities for nonlocal display memory. |
| [_DD_NTCALLBACKS structure](..\ddrawint\ns-ddrawint-_dd_ntcallbacks.md) | The DD_NTCALLBACKS structure contains entry pointers to Microsoft Windows 2000 and later Microsoft DirectDraw callback functions that a device driver supports. |
| [_DD_PALETTE_GLOBAL structure](..\ddrawint\ns-ddrawint-_dd_palette_global.md) | The DD_PALETTE_GLOBAL structure contains the global DirectDrawPalette data that can be shared between object instances. |
| [_DD_PALETTE_LOCAL structure](..\ddrawint\ns-ddrawint-_dd_palette_local.md) | The DD_PALETTE_LOCAL structure contains palette-related data that is unique to an individual palette object. |
| [_DD_QUERYMOCOMPSTATUSDATA structure](..\ddrawint\ns-ddrawint-_dd_querymocompstatusdata.md) | The DD_QUERYMOCOMPSTATUSDATA structure contains information required to query the status of the previous frame. |
| [_DD_RENDERMOCOMPDATA structure](..\ddrawint\ns-ddrawint-_dd_rendermocompdata.md) | The DD_RENDERMOCOMPDATA structure contains the information required to render a frame. |
| [_DD_SETCOLORKEYDATA structure](..\ddrawint\ns-ddrawint-_dd_setcolorkeydata.md) | The DD_SETCOLORKEYDATA structure contains information necessary to set the color key value for the specified surface. |
| [_DD_SETENTRIESDATA structure](..\ddrawint\ns-ddrawint-_dd_setentriesdata.md) | The DD_SETENTRIESDATA structure contains information necessary to set palette entries. |
| [_DD_SETEXCLUSIVEMODEDATA structure](..\ddrawint\ns-ddrawint-_dd_setexclusivemodedata.md) | The DD_SETEXCLUSIVEMODEDATA structure contains the exclusive mode notification information. |
| [_DD_SETOVERLAYPOSITIONDATA structure](..\ddrawint\ns-ddrawint-_dd_setoverlaypositiondata.md) | The DD_SETOVERLAYPOSITIONDATA structure contains information necessary to change the display coordinates of an overlay surface. |
| [_DD_SETPALETTEDATA structure](..\ddrawint\ns-ddrawint-_dd_setpalettedata.md) | The DD_SETPALETTEDATA structure contains information necessary to set a palette for a specific surface. |
| [_DD_STEREOMODE structure](..\ddrawint\ns-ddrawint-_dd_stereomode.md) | The DD_STEREOMODE structure is used by the runtime with GUID_DDStereoMode in a DdGetDriverInfo call to query whether the driver supports stereo for a given video display mode. |
| [_DD_SURFACE_GLOBAL structure](..\ddrawint\ns-ddrawint-_dd_surface_global.md) | The DD_SURFACE_GLOBAL structure contains global surface-related data that can be shared between multiple surfaces. |
| [_DD_SURFACE_INT structure](..\ddrawint\ns-ddrawint-_dd_surface_int.md) | The DD_SURFACE_INT structure contains the DirectDrawSurface object's interface information. |
| [_DD_SURFACE_LOCAL structure](..\ddrawint\ns-ddrawint-_dd_surface_local.md) | The DD_SURFACE_LOCAL structure contains surface-related data that is unique to an individual surface object. |
| [_DD_SURFACE_MORE structure](..\ddrawint\ns-ddrawint-_dd_surface_more.md) | The DD_SURFACE_MORE structure contains additional local data for each individual DirectDrawSurface object. |
| [_DD_SYNCSURFACEDATA structure](..\ddrawint\ns-ddrawint-_dd_syncsurfacedata.md) | The DD_SYNCSURFACEDATA structure contains the surface information. |
| [_DD_SYNCVIDEOPORTDATA structure](..\ddrawint\ns-ddrawint-_dd_syncvideoportdata.md) | The DD_SYNCVIDEOPORTDATA structure contains the video port extensions (VPE) object information. |
| [_DD_UNLOCKDATA structure](..\ddrawint\ns-ddrawint-_dd_unlockdata.md) | The DD_UNLOCKDATA structure contains information necessary to do an unlock as defined by Microsoft DirectDraw parameter structures. |
| [_DD_UPDATENONLOCALHEAPDATA structure](..\ddrawint\ns-ddrawint-_dd_updatenonlocalheapdata.md) | The DD_UPDATENONLOCALHEAPDATA structure contains the required heap information. |
| [_DD_UPDATEOVERLAYDATA structure](..\ddrawint\ns-ddrawint-_dd_updateoverlaydata.md) | The DD_UPDATEOVERLAYDATA structure contains information necessary for updating an overlay surface. |
| [_DD_UPDATEVPORTDATA structure](..\ddrawint\ns-ddrawint-_dd_updatevportdata.md) | The DD_UPDATEVPORTDATA structure contains the information required to start, stop, and change the video port extensions (VPE) object. |
| [_DD_VIDEOPORT_LOCAL structure](..\ddrawint\ns-ddrawint-_dd_videoport_local.md) | The DD_VIDEOPORT_LOCAL structure contains video port extensions (VPE)-related data that is unique to an individual Microsoft DirectDraw VPE object. |
| [_DD_VPORTCOLORDATA structure](..\ddrawint\ns-ddrawint-_dd_vportcolordata.md) | The DD_VPORTCOLORDATA structure contains the video port extensions (VPE) object color control information. |
| [_DD_WAITFORVERTICALBLANKDATA structure](..\ddrawint\ns-ddrawint-_dd_waitforverticalblankdata.md) | The DD_WAITFORVERTICALBLANKDATA structure contains information necessary to obtain the monitor's vertical blank information. |
| [_DD_WAITFORVPORTSYNCDATA structure](..\ddrawint\ns-ddrawint-_dd_waitforvportsyncdata.md) | The DD_WAITFORVPORTSYNCDATA structure contains the information required for the driver to synchronize the video port extensions (VPE) object. |
| [_DXAPI_INTERFACE structure](..\dxmini\ns-dxmini-_dxapi_interface.md) | The DXAPI_INTERFACE structure contains the interface callback functions that a video miniport driver implements to support Kernel-Mode Video Transport. |
| [_DX_IRQDATA structure](..\dxmini\ns-dxmini-_dx_irqdata.md) | The DX_IRQDATA structure contains the IRQ information supplied by the driver. |
| [_HEAPALIGNMENT structure](..\dmemmgr\ns-dmemmgr-_heapalignment.md) | The HEAPALIGNMENT structure contains data specifying the alignment requirements for a given display memory heap. |
| [_SURFACEALIGNMENT structure](..\dmemmgr\ns-dmemmgr-_surfacealignment.md) | The SURFACEALIGNMENT structure is used by a display driver to describe the alignment restrictions for a surface being allocated by HeapVidMemAllocAligned. |
| [_VIDEOMEMORY structure](..\ddrawint\ns-ddrawint-_videomemory.md) | The VIDEOMEMORY structure allows the driver to manage its display memory into heaps. |
| [_VIDEOMEMORYINFO structure](..\ddrawint\ns-ddrawint-_videomemoryinfo.md) | The VIDEOMEMORYINFO structure describes the general format of the display's memory. |
| [_VMEMHEAP structure](..\dmemmgr\ns-dmemmgr-_vmemheap.md) | The VMEMHEAP structure contains information about the heap. |
| [tagAdapter structure](..\cloneviewhelper\ns-cloneviewhelper-tagadapter.md) | The Adapter structure describes a graphics adapter. |
| [tagAdapters structure](..\cloneviewhelper\ns-cloneviewhelper-tagadapters.md) | The Adapters structure contains a list of graphics adapters. |
| [tagDisplayMode structure](..\cloneviewhelper\ns-cloneviewhelper-tagdisplaymode.md) | The DisplayMode structure describes a display device. |
| [tagDisplayModes structure](..\cloneviewhelper\ns-cloneviewhelper-tagdisplaymodes.md) | The DisplayModes structure contains a list of display modes. |
| [tagSources structure](..\cloneviewhelper\ns-cloneviewhelper-tagsources.md) | The Sources structure contains a Video Present Network (VidPN) topology. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IDirectDrawKernel::GetCaps](..\ddkernel\nf-ddkernel-idirectdrawkernel-getcaps.md) | The IDirectDrawKernel |
| [IDirectDrawKernel::GetKernelHandle](..\ddkernel\nf-ddkernel-idirectdrawkernel-getkernelhandle.md) | The IDirectDrawKernel |
| [IDirectDrawKernel::ReleaseKernelHandle](..\ddkernel\nf-ddkernel-idirectdrawkernel-releasekernelhandle.md) | The IDirectDrawKernel |
| [IDirectDrawSurfaceKernel::GetKernelHandle](..\ddkernel\nf-ddkernel-idirectdrawsurfacekernel-getkernelhandle.md) | The IDirectDrawSurfaceKernel |
| [IDirectDrawSurfaceKernel::ReleaseKernelHandle](..\ddkernel\nf-ddkernel-idirectdrawsurfacekernel-releasekernelhandle.md) | The IDirectDrawSurfaceKernel |
| [IViewHelper::Commit](..\cloneviewhelper\nf-cloneviewhelper-iviewhelper-commit.md) | The Commit method invalidates a Video Present Network (VidPN) on all graphics adapters. |
| [IViewHelper::GetActiveTopology](..\cloneviewhelper\nf-cloneviewhelper-iviewhelper-getactivetopology.md) | The GetActiveTopology method retrieves, for a given adapter, an array of identifiers for targets that are active on a given source. |
| [IViewHelper::GetConnectedIDs](..\cloneviewhelper\nf-cloneviewhelper-iviewhelper-getconnectedids.md) | The GetConnectedIDs method retrieves, for a given adapter, an array of identifiers for either targets or sources. |
| [IViewHelper::GetProceedOnNewConfiguration](..\cloneviewhelper\nf-cloneviewhelper-iviewhelper-getproceedonnewconfiguration.md) | The GetProceedOnNewConfiguration method allows the user-mode display driver to suppress the TMM user interface and display changing actions on a new, two-monitor configuration. |
| [IViewHelper::SetActiveTopology](..\cloneviewhelper\nf-cloneviewhelper-iviewhelper-setactivetopology.md) | The SetActiveTopology method sets up the topology to be used by a Video Present Network (VidPN) on a particular graphics adapter. |
| [IViewHelper::SetConfiguration](..\cloneviewhelper\nf-cloneviewhelper-iviewhelper-setconfiguration.md) | The SetConfiguration method passes in display data (display modes and topology data) to the underlying user-mode display driver that the driver should set. |
