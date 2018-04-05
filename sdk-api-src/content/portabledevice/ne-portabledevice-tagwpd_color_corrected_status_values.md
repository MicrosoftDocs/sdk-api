---
UID: NE:portabledevice.tagWPD_COLOR_CORRECTED_STATUS_VALUES
title: tagWPD_COLOR_CORRECTED_STATUS_VALUES
author: windows-driver-content
description: The WPD_COLOR_CORRECTED_STATUS_VALUES enumeration type describes the color correction status of an image or video file.
old-location: wpdsdk\wpd_color_corrected_status_values.htm
old-project: wpd_sdk
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_COLOR_CORRECTED_STATUS_CORRECTED, WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED, WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED, WPD_COLOR_CORRECTED_STATUS_VALUES, WPD_COLOR_CORRECTED_STATUS_VALUES enumeration [Windows Portable Devices SDK], enumeration [Windows Portable Devices SDK], portabledevice/WPD_COLOR_CORRECTED_STATUS_CORRECTED, portabledevice/WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED, portabledevice/WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED, portabledevice/WPD_COLOR_CORRECTED_STATUS_VALUES, tagWPD_COLOR_CORRECTED_STATUS_VALUES, wpdsdk.wpd_color_corrected_status_values
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
req.typenames: WPD_COLOR_CORRECTED_STATUS_VALUES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_COLOR_CORRECTED_STATUS_VALUES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_COLOR_CORRECTED_STATUS_VALUES enumeration


## -description



        The <b>WPD_COLOR_CORRECTED_STATUS_VALUES</b> enumeration type describes the color correction status of an image or video file.
      


## -enum-fields




### -field WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED


            The image has not been color corrected.
          


### -field WPD_COLOR_CORRECTED_STATUS_CORRECTED


            The image has been color corrected.
          


### -field WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED


            The image has not been, and should not be, color corrected.
          


## -remarks




        Indicates the color corrected status of an image. This enumeration is used by the <a href="image_properties.htm">WPD_IMAGE_COLOR_CORRECTED_STATUS</a> property.
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

