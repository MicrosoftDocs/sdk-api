---
UID: NS:winddi._GAMMARAMP
title: GAMMARAMP (winddi.h)
author: windows-sdk-content
description: The GAMMARAMP structure is used by DrvIcmSetDeviceGammaRamp to set the hardware gamma ramp of a particular display device.
old-location: display\gammaramp.htm
tech.root: display
ms.assetid: cc082911-5089-4335-93d2-1405ca390741
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PGAMMARAMP, GAMMARAMP, GAMMARAMP structure [Display Devices], PGAMMARAMP, PGAMMARAMP structure pointer [Display Devices], display.gammaramp, grstrcts_fdf8b6b9-dfc1-4679-b461-58488eb5d9b4.xml, winddi/GAMMARAMP, winddi/PGAMMARAMP"
ms.topic: struct
req.header: winddi.h
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
 - winddi.h
api_name:
 - GAMMARAMP
product: Windows
targetos: Windows
req.typenames: GAMMARAMP, *PGAMMARAMP
req.redist: 
---

# GAMMARAMP structure


## -description


The GAMMARAMP structure is used by <a href="https://msdn.microsoft.com/0ea0c60c-fa12-4dd0-a6cc-45eacf4b73c0">DrvIcmSetDeviceGammaRamp</a> to set the hardware <a href="https://msdn.microsoft.com/f67c673d-c6f0-49f0-850a-d8b00e99ddd4">gamma ramp</a> of a particular display device. 


## -struct-fields




### -field Red

Is the 256-entry ramp for the red color channel.


### -field Green

Is the 256-entry ramp for the green color channel.


### -field Blue

Is the 256-entry ramp for the blue color channel.


## -see-also




<a href="https://msdn.microsoft.com/0ea0c60c-fa12-4dd0-a6cc-45eacf4b73c0">DrvIcmSetDeviceGammaRamp</a>
 

 

