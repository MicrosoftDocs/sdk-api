---
UID: NS:winddi._GAMMARAMP
title: GAMMARAMP (winddi.h)
description: The GAMMARAMP structure is used by DrvIcmSetDeviceGammaRamp to set the hardware gamma ramp of a particular display device.
helpviewer_keywords: ["*PGAMMARAMP","GAMMARAMP","GAMMARAMP structure [Display Devices]","PGAMMARAMP","PGAMMARAMP structure pointer [Display Devices]","display.gammaramp","grstrcts_fdf8b6b9-dfc1-4679-b461-58488eb5d9b4.xml","winddi/GAMMARAMP","winddi/PGAMMARAMP"]
old-location: display\gammaramp.htm
tech.root: display
ms.assetid: cc082911-5089-4335-93d2-1405ca390741
ms.date: 12/05/2018
ms.keywords: '*PGAMMARAMP, GAMMARAMP, GAMMARAMP structure [Display Devices], PGAMMARAMP, PGAMMARAMP structure pointer [Display Devices], display.gammaramp, grstrcts_fdf8b6b9-dfc1-4679-b461-58488eb5d9b4.xml, winddi/GAMMARAMP, winddi/PGAMMARAMP'
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
targetos: Windows
req.typenames: GAMMARAMP, *PGAMMARAMP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GAMMARAMP
 - winddi/_GAMMARAMP
 - PGAMMARAMP
 - winddi/PGAMMARAMP
 - GAMMARAMP
 - winddi/GAMMARAMP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - GAMMARAMP
---

# GAMMARAMP structure


## -description

The GAMMARAMP structure is used by <a href="/windows/desktop/api/winddi/nf-winddi-drvicmsetdevicegammaramp">DrvIcmSetDeviceGammaRamp</a> to set the hardware <a href="/windows-hardware/drivers/">gamma ramp</a> of a particular display device.

## -struct-fields

### -field Red

Is the 256-entry ramp for the red color channel.

### -field Green

Is the 256-entry ramp for the green color channel.

### -field Blue

Is the 256-entry ramp for the blue color channel.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvicmsetdevicegammaramp">DrvIcmSetDeviceGammaRamp</a>