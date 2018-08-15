---
UID: NC:ddrawint.PDD_MAPMEMORY
title: PDD_MAPMEMORY
author: windows-sdk-content
description: The DdMapMemory callback function maps application-modifiable portions of the frame buffer into the user-mode address space of the specified process, or unmaps memory.
old-location: display\ddmapmemory.htm
old-project: display
ms.assetid: a05e2ba8-dfe1-447d-acfa-0eb8f4252107
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DdMapMemory, DdMapMemory callback function [Display Devices], PDD_MAPMEMORY, PDD_MAPMEMORY callback, ddfncs_565a064a-cd87-4f20-8478-05176ce57ad8.xml, ddrawint/DdMapMemory, display.ddmapmemory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
req.redist: 
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
tech.root: 
req.typenames: "*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA"
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
req.lib: 
req.dll: 
req.irql: 
---

# PDD_MAPMEMORY callback function


## -description


The <b>DdMapMemory</b> callback function maps application-modifiable portions of the frame buffer into the user-mode address space of the specified process, or unmaps memory.


## -parameters




### -param Arg1








#### - lpMapMemory

Points to a <a href="https://msdn.microsoft.com/51d8b35f-883c-4e47-a0e6-af6c8ade8e54">DD_MAPMEMORYDATA</a> structure that contains details for the memory mapping or unmapping operation.


## -returns



<b>DdMapMemory</b> returns one of the following callback codes:




## -remarks



<b>DdMapMemory</b> is called to perform memory mapping before the first call to <a href="https://msdn.microsoft.com/b5256ed8-79be-4c7b-a079-ed3bca954e9e">DdLock</a>. The handle returned by the driver in the <b>fpProcess</b> member of the <a href="https://msdn.microsoft.com/51d8b35f-883c-4e47-a0e6-af6c8ade8e54">DD_MAPMEMORYDATA</a> structure at <i>lpMapMemory</i> will be passed to every <i>DdLock</i> call made on the driver. 

<b>DdMapMemory</b> is also called to unmap memory after the last <a href="https://msdn.microsoft.com/dbb7b34c-5473-42b9-b16f-e71b9c3e1db8">DdUnlock</a> call is made.

To prevent driver crashes, the driver must not map any portion of the frame buffer that must not be modified by an application.

The display driver must call upon the <a href="https://msdn.microsoft.com/3a540bfe-f340-4f12-acee-323b97683074">video miniport driver</a> to perform the memory mapping or unmapping. To send a synchronous request to the video miniport driver to map the memory, the display driver calls the <a href="https://msdn.microsoft.com/a38186b6-4b27-4360-8721-49c95dd94806">EngDeviceIoControl</a> GDI function with <a href="https://msdn.microsoft.com/7e2e437c-d244-4799-abfc-35fb9d2196d7">IOCTL_VIDEO_SHARE_VIDEO_MEMORY</a> or <a href="https://msdn.microsoft.com/9e17502a-b5bf-4f17-8e74-1974f7e65e01">IOCTL_VIDEO_MAP_VIDEO_MEMORY</a>. The display driver sends <a href="https://msdn.microsoft.com/f6ec4237-05f1-4777-a035-7cedb4283e0e">IOCTL_VIDEO_UNSHARE_VIDEO_MEMORY</a> or <a href="https://msdn.microsoft.com/421cbe15-f2a6-495d-90f2-09a13771d018">IOCTL_VIDEO_UNMAP_VIDEO_MEMORY</a> to the video miniport driver to unmap the memory. For more information, see <a href="https://msdn.microsoft.com/9f9ad20e-d8cf-485d-adad-c04eeb40b705">Communicating IOCTLs to the Video Miniport Driver</a>.

<b>DdMapMemory</b> can only be called with a disabled <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> to unmap memory. A PDEV is disabled or enabled by calling the display driver's <a href="https://msdn.microsoft.com/29846ffd-b721-4d61-9983-07a2575f9fe8">DrvAssertMode</a> function. See <a href="https://msdn.microsoft.com/f7badbe8-b24f-438a-8937-95bb98de6310">Managing PDEVs</a> for more information. 




## -see-also




<a href="https://msdn.microsoft.com/51d8b35f-883c-4e47-a0e6-af6c8ade8e54">DD_MAPMEMORYDATA</a>



<a href="https://msdn.microsoft.com/b5256ed8-79be-4c7b-a079-ed3bca954e9e">DdLock</a>



<a href="https://msdn.microsoft.com/dbb7b34c-5473-42b9-b16f-e71b9c3e1db8">DdUnlock</a>



<a href="https://msdn.microsoft.com/a38186b6-4b27-4360-8721-49c95dd94806">EngDeviceIoControl</a>



<a href="https://msdn.microsoft.com/9e17502a-b5bf-4f17-8e74-1974f7e65e01">IOCTL_VIDEO_MAP_VIDEO_MEMORY</a>



<a href="https://msdn.microsoft.com/7e2e437c-d244-4799-abfc-35fb9d2196d7">IOCTL_VIDEO_SHARE_VIDEO_MEMORY</a>



<a href="https://msdn.microsoft.com/421cbe15-f2a6-495d-90f2-09a13771d018">IOCTL_VIDEO_UNMAP_VIDEO_MEMORY</a>



<a href="https://msdn.microsoft.com/f6ec4237-05f1-4777-a035-7cedb4283e0e">IOCTL_VIDEO_UNSHARE_VIDEO_MEMORY</a>
 

 

