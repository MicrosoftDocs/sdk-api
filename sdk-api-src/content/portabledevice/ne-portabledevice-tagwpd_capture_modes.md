---
UID: NE:portabledevice.tagWPD_CAPTURE_MODES
title: tagWPD_CAPTURE_MODES
author: windows-driver-content
description: The WPD_CAPTURE_MODES enumeration type describes the capture timing mode of a still image capture.
old-location: wpdsdk\wpd_capture_modes.htm
old-project: wpd_sdk
ms.assetid: bfe96176-d018-4b39-a938-035757111784
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_CAPTURE_MODES, WPD_CAPTURE_MODES enumeration [Windows Portable Devices SDK], WPD_CAPTURE_MODE_BURST, WPD_CAPTURE_MODE_NORMAL, WPD_CAPTURE_MODE_TIMELAPSE, WPD_CAPTURE_MODE_UNDEFINED, enumeration [Windows Portable Devices SDK], portabledevice/WPD_CAPTURE_MODES, portabledevice/WPD_CAPTURE_MODE_BURST, portabledevice/WPD_CAPTURE_MODE_NORMAL, portabledevice/WPD_CAPTURE_MODE_TIMELAPSE, portabledevice/WPD_CAPTURE_MODE_UNDEFINED, tagWPD_CAPTURE_MODES, wpdsdk.wpd_capture_modes
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
req.typenames: WPD_CAPTURE_MODES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_CAPTURE_MODES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_CAPTURE_MODES enumeration


## -description



        The <b>WPD_CAPTURE_MODES</b> enumeration type describes the capture timing mode of a still image capture.
      


## -enum-fields




### -field WPD_CAPTURE_MODE_UNDEFINED


            The capture mode has not been defined.
          


### -field WPD_CAPTURE_MODE_NORMAL


            No delay or burst mode should be used.
          


### -field WPD_CAPTURE_MODE_BURST


            Specifies that a defined number of images should be captured with a defined interval between them. The number of images to capture and time delay between them are specified by the <a href="still_image_properties.htm">WPD_STILL_IMAGE_BURST_NUMBER</a> and <a href="still_image_properties.htm">WPD_STILL_IMAGE_BURST_INTERVAL</a> properties.
          


### -field WPD_CAPTURE_MODE_TIMELAPSE


            Image capture should use time lapse photography. The number of images and interval between them are described by the <a href="still_image_properties.htm">WPD_STILL_IMAGE_TIMELAPSE_NUMBER</a> and <a href="still_image_properties.htm">WPD_STILL_IMAGE_TIMELAPSE_INTERVAL</a> properties.
          


## -remarks




        This enumeration is used by the <a href="still_image_properties.htm">WPD_STILL_IMAGE_CAPTURE_MODE</a> property.
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff597900">WPD Properties and Attributes</a>
 

 

