---
UID: NS:ddrawint.DD_CALLBACKS
title: DD_CALLBACKS
author: windows-sdk-content
description: The DD_CALLBACKS structure contains entry pointers to the callback functions that a device driver supports.
old-location: display\dd_callbacks.htm
tech.root: display
ms.assetid: d68b2772-dca6-417a-8e03-d3b2843fb69d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PDD_CALLBACKS, DD_CALLBACKS, DD_CALLBACKS structure [Display Devices], ddrawint/DD_CALLBACKS, ddstrcts_c4da6934-e140-40db-b7dc-686c205cb877.xml, display.dd_callbacks"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_CALLBACKS
product: Windows
targetos: Windows
req.typenames: DD_CALLBACKS
req.redist: 
---

# DD_CALLBACKS structure


## -description


The DD_CALLBACKS structure contains entry pointers to the callback functions that a device driver supports.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this structure.


### -field dwFlags

Indicates what Microsoft DirectDraw callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_CB32_CANCREATESURFACE</dt>
<dt>DDHAL_CB32_CREATEPALETTE</dt>
<dt>DDHAL_CB32_CREATESURFACE</dt>
<dt>DDHAL_CB32_GETSCANLINE</dt>
<dt>DDHAL_CB32_MAPMEMORY</dt>
<dt>DDHAL_CB32_SETCOLORKEY</dt>
<dt>DDHAL_CB32_SETMODE</dt>
<dt>DDHAL_CB32_WAITFORVERTICALBLANK</dt>
</dl>



### -field DestroyDriver

Unused on Microsoft Windows 2000 and later and should be ignored by the driver.


### -field CreateSurface

Points to the driver-supplied <a href="https://msdn.microsoft.com/45c793ed-34e8-4a15-91f4-9a258c1842fd">DdCreateSurface</a> callback.


### -field SetColorKey

Points to the driver-supplied <a href="https://msdn.microsoft.com/4b4ee889-15c8-4a7c-a9d8-adab27b271dd">DdSetColorKey</a> callback.


### -field SetMode

Unused on Windows 2000 and later and should be ignored by the driver.


### -field WaitForVerticalBlank

Points to the driver-supplied <a href="https://msdn.microsoft.com/0eeeed70-bfda-45c0-8709-29e97ab0c5a9">DdWaitForVerticalBlank</a> callback.


### -field CanCreateSurface

Points to the driver-supplied <a href="https://msdn.microsoft.com/015b94d7-427f-401d-b348-d4e9ec5cfe5d">DdCanCreateSurface</a> callback.


### -field CreatePalette

Points to the driver-supplied <a href="https://msdn.microsoft.com/047d63c6-eb4c-4944-8c98-0f9686e2c37a">DdCreatePalette</a> callback.


### -field GetScanLine

Points to the driver-supplied <a href="https://msdn.microsoft.com/3738205f-2d27-4211-944a-6ca71954fe47">DdGetScanLine</a> callback.


### -field MapMemory

Points to the driver-supplied <a href="https://msdn.microsoft.com/a05e2ba8-dfe1-447d-acfa-0eb8f4252107">DdMapMemory</a> callback.


## -remarks



Entries that the display driver does not use should be set to <b>NULL</b>. GDI allocates the memory for this structure and calls the driver's <a href="https://msdn.microsoft.com/eb7e8775-d0ff-42af-8266-5171902eac22">DrvEnableDirectDraw</a> function to initialize it.




## -see-also




<a href="https://msdn.microsoft.com/fcf0e136-a7cc-4bb3-8af4-2478d4a2c055">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/85dcb71b-ad1f-4b83-8ead-db502d9f294e">DD_KERNELCALLBACKS</a>



<a href="https://msdn.microsoft.com/9bf47408-cc7f-455d-bbb2-6f1f318eee5f">DD_MISCELLANEOUSCALLBACKS</a>



<a href="https://msdn.microsoft.com/db707fd8-2190-4c4f-89fd-ab46d97f66a2">DD_MOTIONCOMPCALLBACKS</a>



<a href="https://msdn.microsoft.com/9d226b1c-6959-4cc8-9e60-b57a324d9a8a">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/742b03b0-f729-489c-a87f-b8eb404b6290">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/a363446e-a9f7-4b32-acc2-c369d3dfe8f3">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/5e03d240-f483-4ecf-8890-b9f0368e2b2f">DD_VIDEOPORTCALLBACKS</a>



<a href="https://msdn.microsoft.com/eb7e8775-d0ff-42af-8266-5171902eac22">DrvEnableDirectDraw</a>
 

 

