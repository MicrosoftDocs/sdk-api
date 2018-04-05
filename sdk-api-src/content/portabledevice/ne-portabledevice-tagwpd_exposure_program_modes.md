---
UID: NE:portabledevice.tagWPD_EXPOSURE_PROGRAM_MODES
title: tagWPD_EXPOSURE_PROGRAM_MODES
author: windows-driver-content
description: The WPD_EXPOSURE_PROGRAM_MODES enumeration type describes an exposure mode to use when capturing images with a device.
old-location: wpdsdk\wpd_exposure_program_modes.htm
old-project: wpd_sdk
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_EXPOSURE_PROGRAM_MODES, WPD_EXPOSURE_PROGRAM_MODES enumeration [Windows Portable Devices SDK], WPD_EXPOSURE_PROGRAM_MODE_ACTION, WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY, WPD_EXPOSURE_PROGRAM_MODE_AUTO, WPD_EXPOSURE_PROGRAM_MODE_CREATIVE, WPD_EXPOSURE_PROGRAM_MODE_MANUAL, WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT, WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY, WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED, enumeration [Windows Portable Devices SDK], portabledevice/WPD_EXPOSURE_PROGRAM_MODES, portabledevice/WPD_EXPOSURE_PROGRAM_MODE_ACTION, portabledevice/WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY, portabledevice/WPD_EXPOSURE_PROGRAM_MODE_AUTO, portabledevice/WPD_EXPOSURE_PROGRAM_MODE_CREATIVE, portabledevice/WPD_EXPOSURE_PROGRAM_MODE_MANUAL, portabledevice/WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT, portabledevice/WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY, portabledevice/WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED, tagWPD_EXPOSURE_PROGRAM_MODES, wpdsdk.wpd_exposure_program_modes
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
req.typenames: WPD_EXPOSURE_PROGRAM_MODES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_EXPOSURE_PROGRAM_MODES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_EXPOSURE_PROGRAM_MODES enumeration


## -description



        The <b>WPD_EXPOSURE_PROGRAM_MODES</b> enumeration type describes an exposure mode to use when capturing images with a device.
      


## -enum-fields




### -field WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED


            The exposure mode has not been specified.
          


### -field WPD_EXPOSURE_PROGRAM_MODE_MANUAL


            The application should specify all exposure settings.
          


### -field WPD_EXPOSURE_PROGRAM_MODE_AUTO


            Use a device-defined automatic exposure mode.
          


### -field WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY


            An automated exposure mode that indicates that the lens aperture value should remain fixed, but shutter speed should be determined by the device.
          


### -field WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY


            An automated exposure mode that indicates that the shutter speed should remain fixed, but that lens aperture should be determined by the device.
          


### -field WPD_EXPOSURE_PROGRAM_MODE_CREATIVE


            An automated exposure mode that tries to maximize the depth of field.
          


### -field WPD_EXPOSURE_PROGRAM_MODE_ACTION


            An automated exposure mode that tries to maximize the shutter speed.
          


### -field WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT


            An automated exposure mode that specifies a relatively shallow depth of field.
          


## -remarks




        Indicates the exposure program mode of the device. This enumeration is used by the <a href="still_image_properties.htm">WPD_STILL_IMAGE_EXPOSURE_PROGRAM_MODE</a> property.
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

