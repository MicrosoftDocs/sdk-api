---
UID: NE:portabledevice.tagWPD_EXPOSURE_METERING_MODES
title: tagWPD_EXPOSURE_METERING_MODES
author: windows-driver-content
description: The WPD_EXPOSURE_METERING_MODES enumeration type describes the metering mode to use when estimating exposure for still image capture by a device.
old-location: wpdsdk\wpd_exposure_metering_modes.htm
old-project: wpd_sdk
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_EXPOSURE_METERING_MODES, WPD_EXPOSURE_METERING_MODES enumeration [Windows Portable Devices SDK], WPD_EXPOSURE_METERING_MODE_AVERAGE, WPD_EXPOSURE_METERING_MODE_CENTER_SPOT, WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE, WPD_EXPOSURE_METERING_MODE_MULTI_SPOT, WPD_EXPOSURE_METERING_MODE_UNDEFINED, enumeration [Windows Portable Devices SDK], portabledevice/WPD_EXPOSURE_METERING_MODES, portabledevice/WPD_EXPOSURE_METERING_MODE_AVERAGE, portabledevice/WPD_EXPOSURE_METERING_MODE_CENTER_SPOT, portabledevice/WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE, portabledevice/WPD_EXPOSURE_METERING_MODE_MULTI_SPOT, portabledevice/WPD_EXPOSURE_METERING_MODE_UNDEFINED, tagWPD_EXPOSURE_METERING_MODES, wpdsdk.wpd_exposure_metering_modes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: portabledevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WPD_EXPOSURE_METERING_MODES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_EXPOSURE_METERING_MODES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_EXPOSURE_METERING_MODES enumeration


## -description



        The <b>WPD_EXPOSURE_METERING_MODES</b> enumeration type describes the metering mode to use when estimating exposure for still image capture by a device.
      


## -enum-fields




### -field WPD_EXPOSURE_METERING_MODE_UNDEFINED


            The metering mode is undefined.
          


### -field WPD_EXPOSURE_METERING_MODE_AVERAGE


            Use averaged exposure across the full image.
          


### -field WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE


            Use an averaged exposure, with the center of the image given more weight.
          


### -field WPD_EXPOSURE_METERING_MODE_MULTI_SPOT


            Use a multi-spot averaging technique.
          


### -field WPD_EXPOSURE_METERING_MODE_CENTER_SPOT


            Use a center-spot averaging technique.
          


## -remarks




        Indicates the metering mode of the device. This enumeration is used by the <a href="still_image_properties.htm">WPD_STILL_IMAGE_EXPOSURE_METERING_MODE</a> property.
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

