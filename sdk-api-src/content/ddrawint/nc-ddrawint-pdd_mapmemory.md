---
UID: NC:ddrawint.PDD_MAPMEMORY
title: PDD_MAPMEMORY (ddrawint.h)
author: windows-sdk-content
description: The DdMapMemory callback function maps application-modifiable portions of the frame buffer into the user-mode address space of the specified process, or unmaps memory.
old-location: display\ddmapmemory.htm
tech.root: display
ms.assetid: a05e2ba8-dfe1-447d-acfa-0eb8f4252107
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DdMapMemory, DdMapMemory callback function [Display Devices], PDD_MAPMEMORY, PDD_MAPMEMORY callback, ddfncs_565a064a-cd87-4f20-8478-05176ce57ad8.xml, ddrawint/DdMapMemory, display.ddmapmemory
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdMapMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDD_MAPMEMORY callback function


## -description


The <b>DdMapMemory</b> callback function maps application-modifiable portions of the frame buffer into the user-mode address space of the specified process, or unmaps memory.


## -parameters




### -param Arg1








#### - lpMapMemory

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-_dd_mapmemorydata">DD_MAPMEMORYDATA</a> structure that contains details for the memory mapping or unmapping operation.


## -returns



<b>DdMapMemory</b> returns one of the following callback codes:




## -remarks



<b>DdMapMemory</b> is called to perform memory mapping before the first call to <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_lock">DdLock</a>. The handle returned by the driver in the <b>fpProcess</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-_dd_mapmemorydata">DD_MAPMEMORYDATA</a> structure at <i>lpMapMemory</i> will be passed to every <i>DdLock</i> call made on the driver. 

<b>DdMapMemory</b> is also called to unmap memory after the last <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_unlock">DdUnlock</a> call is made.

To prevent driver crashes, the driver must not map any portion of the frame buffer that must not be modified by an application.

The display driver must call upon the <a href="https://docs.microsoft.com/windows-hardware/drivers/display/video-miniport-drivers-in-the-windows-2000-display-driver-model">video miniport driver</a> to perform the memory mapping or unmapping. To send a synchronous request to the video miniport driver to map the memory, the display driver calls the <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engdeviceiocontrol">EngDeviceIoControl</a> GDI function with <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntddvdeo/ni-ntddvdeo-ioctl_video_share_video_memory">IOCTL_VIDEO_SHARE_VIDEO_MEMORY</a> or <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntddvdeo/ni-ntddvdeo-ioctl_video_map_video_memory">IOCTL_VIDEO_MAP_VIDEO_MEMORY</a>. The display driver sends <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntddvdeo/ni-ntddvdeo-ioctl_video_unshare_video_memory">IOCTL_VIDEO_UNSHARE_VIDEO_MEMORY</a> or <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntddvdeo/ni-ntddvdeo-ioctl_video_unmap_video_memory">IOCTL_VIDEO_UNMAP_VIDEO_MEMORY</a> to the video miniport driver to unmap the memory. For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/display/communicating-ioctls-to-the-video-miniport-driver">Communicating IOCTLs to the Video Miniport Driver</a>.

<b>DdMapMemory</b> can only be called with a disabled <a href="https://docs.microsoft.com/windows-hardware/drivers/">PDEV</a> to unmap memory. A PDEV is disabled or enabled by calling the display driver's <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvassertmode">DrvAssertMode</a> function. See <a href="https://docs.microsoft.com/windows-hardware/drivers/display/managing-pdevs">Managing PDEVs</a> for more information. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-_dd_mapmemorydata">DD_MAPMEMORYDATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_lock">DdLock</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_unlock">DdUnlock</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engdeviceiocontrol">EngDeviceIoControl</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntddvdeo/ni-ntddvdeo-ioctl_video_map_video_memory">IOCTL_VIDEO_MAP_VIDEO_MEMORY</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntddvdeo/ni-ntddvdeo-ioctl_video_share_video_memory">IOCTL_VIDEO_SHARE_VIDEO_MEMORY</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntddvdeo/ni-ntddvdeo-ioctl_video_unmap_video_memory">IOCTL_VIDEO_UNMAP_VIDEO_MEMORY</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntddvdeo/ni-ntddvdeo-ioctl_video_unshare_video_memory">IOCTL_VIDEO_UNSHARE_VIDEO_MEMORY</a>
 

 

