---
UID: NE:portabledevice.tagWPD_WHITE_BALANCE_SETTINGS
title: tagWPD_WHITE_BALANCE_SETTINGS
author: windows-driver-content
description: The WPD_WHITE_BALANCE_SETTINGS enumeration type describes how a video or image device weights color channels to achieve a proper white balance.
old-location: wpdsdk\wpd_white_balance_settings.htm
old-project: wpd_sdk
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_WHITE_BALANCE_AUTOMATIC, WPD_WHITE_BALANCE_DAYLIGHT, WPD_WHITE_BALANCE_FLASH, WPD_WHITE_BALANCE_MANUAL, WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC, WPD_WHITE_BALANCE_SETTINGS, WPD_WHITE_BALANCE_SETTINGS enumeration [Windows Portable Devices SDK], WPD_WHITE_BALANCE_TUNGSTEN, WPD_WHITE_BALANCE_UNDEFINED, enumeration [Windows Portable Devices SDK], portabledevice/WPD_WHITE_BALANCE_AUTOMATIC, portabledevice/WPD_WHITE_BALANCE_DAYLIGHT, portabledevice/WPD_WHITE_BALANCE_FLASH, portabledevice/WPD_WHITE_BALANCE_MANUAL, portabledevice/WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC, portabledevice/WPD_WHITE_BALANCE_SETTINGS, portabledevice/WPD_WHITE_BALANCE_TUNGSTEN, portabledevice/WPD_WHITE_BALANCE_UNDEFINED, tagWPD_WHITE_BALANCE_SETTINGS, wpdsdk.wpd_white_balance_settings
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
req.typenames: WPD_WHITE_BALANCE_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_WHITE_BALANCE_SETTINGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_WHITE_BALANCE_SETTINGS enumeration


## -description



        The <b>WPD_WHITE_BALANCE_SETTINGS</b> enumeration type describes how a video or image device weights color channels to achieve a proper white balance.
      


## -enum-fields




### -field WPD_WHITE_BALANCE_UNDEFINED


            This value has not been defined.
          


### -field WPD_WHITE_BALANCE_MANUAL


            The white balance is set explicitly by using the <a href="still_image_properties.htm">WPD_STILL_IMAGE_RGB_GAIN</a> property and will not change by itself.
          


### -field WPD_WHITE_BALANCE_AUTOMATIC


            The device will set the white balance.
          


### -field WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC


            The device will set the white balance, but only when the user pushes the device's capture button while aiming the device at a white field.
          


### -field WPD_WHITE_BALANCE_DAYLIGHT


            The device will use white balance numbers appropriate for use in most daylight settings.
          


### -field WPD_WHITE_BALANCE_FLORESCENT


### -field WPD_WHITE_BALANCE_TUNGSTEN


            The device will use white balance numbers appropriate for use in most indoor, incandescent lighting settings.
          


### -field WPD_WHITE_BALANCE_FLASH


            The device will use white balance numbers appropriate for use with a flash.
          


## -remarks




        This enumeration is used by the <a href="still_image_properties.htm">WPD_STILL_IMAGE_WHITE_BALANCE</a> property.
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

