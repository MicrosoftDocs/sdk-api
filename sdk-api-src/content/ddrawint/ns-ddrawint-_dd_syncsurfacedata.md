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

# _DD_SYNCSURFACEDATA structure


## -description


The DD_SYNCSURFACEDATA structure contains the surface information. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpDDSurface

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure that describes the surface with which to sync. 


### -field dwSurfaceOffset

Contains the byte offset from the start of the frame buffer to the start of the surface. This value is used only by the video miniport driver. This member must contain data that is filled in by the driver. 


### -field fpLockPtr

Contains the pointer value to be returned by the <a href="https://msdn.microsoft.com/b5256ed8-79be-4c7b-a079-ed3bca954e9e">DdLock</a> call for accessing the surface. This value is used by a kernel-mode client. This member can be modified by the driver, but does not need to be. 


### -field lPitch

Contains the pitch in bytes passed to the client during a <a href="https://msdn.microsoft.com/b5256ed8-79be-4c7b-a079-ed3bca954e9e">DdLock</a> call. This member can be modified by the driver, but does not need to be. 


### -field dwOverlayOffset

Contains the byte offset from the start of the frame buffer to the start of the overlay. This value is used only by the video miniport driver and may be different than the <b>dwSurfaceOffset</b> member if cropping is involved or if the overlay origin is not the top left of the surface. This member must contain data that is filled in by the driver. 


### -field dwDriverReserved1

Reserved for use by the display driver.


### -field dwDriverReserved2

Reserved for use by the display driver.


### -field dwDriverReserved3

Reserved for use by the display driver.


### -field dwDriverReserved4

Reserved for use by the display driver. Windows 2000 and later only.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/730e0fd4-aaae-4de7-86d5-fa2145be3cd1">DdSyncSurfaceData</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/b5256ed8-79be-4c7b-a079-ed3bca954e9e">DdLock</a>



<a href="https://msdn.microsoft.com/730e0fd4-aaae-4de7-86d5-fa2145be3cd1">DdSyncSurfaceData</a>
 

 

