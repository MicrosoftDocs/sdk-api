---
UID: NE:portabledevice.tagWPD_CROPPED_STATUS_VALUES
title: tagWPD_CROPPED_STATUS_VALUES
author: windows-driver-content
description: The WPD_CROPPED_STATUS_VALUES enumeration type describes the cropping status of an image.
old-location: wpdsdk\wpd_cropped_status_values.htm
old-project: wpd_sdk
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_CROPPED_STATUS_CROPPED, WPD_CROPPED_STATUS_NOT_CROPPED, WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED, WPD_CROPPED_STATUS_VALUES, WPD_CROPPED_STATUS_VALUES enumeration [Windows Portable Devices SDK], enumeration [Windows Portable Devices SDK], portabledevice/WPD_CROPPED_STATUS_CROPPED, portabledevice/WPD_CROPPED_STATUS_NOT_CROPPED, portabledevice/WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED, portabledevice/WPD_CROPPED_STATUS_VALUES, tagWPD_CROPPED_STATUS_VALUES, wpdsdk.wpd_cropped_status_values
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
req.typenames: WPD_CROPPED_STATUS_VALUES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_CROPPED_STATUS_VALUES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_CROPPED_STATUS_VALUES enumeration


## -description



        The <b>WPD_CROPPED_STATUS_VALUES</b> enumeration type describes the cropping status of an image.
      


## -enum-fields




### -field WPD_CROPPED_STATUS_NOT_CROPPED


            The image has not been cropped.
          


### -field WPD_CROPPED_STATUS_CROPPED


            The image has been cropped.
          


### -field WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED


            The image has not been, and should not be, cropped.
          


## -remarks




        Indicates the cropped status of an image. This enumeration is used by the <a href="image_properties.htm">WPD_IMAGE_CROPPED_STATUS</a> property.
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

