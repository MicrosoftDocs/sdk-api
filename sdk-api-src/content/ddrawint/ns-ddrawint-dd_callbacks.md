---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



Entries that the display driver does not use should be set to <b>NULL</b>. GDI allocates the memory for this structure and calls the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556208">DrvEnableDirectDraw</a> function to initialize it.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550521">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551633">DD_KERNELCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551657">DD_MISCELLANEOUSCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551660">DD_MOTIONCOMPCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551673">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551681">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551721">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551758">DD_VIDEOPORTCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556208">DrvEnableDirectDraw</a>
 

 

