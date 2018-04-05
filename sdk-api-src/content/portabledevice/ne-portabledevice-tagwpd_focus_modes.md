---
UID: NE:portabledevice.tagWPD_FOCUS_MODES
title: tagWPD_FOCUS_MODES
author: windows-driver-content
description: The WPD_FOCUS_MODES enumeration type describes the focus mode used by a still image capture device.
old-location: wpdsdk\wpd_focus_modes.htm
old-project: wpd_sdk
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_FOCUS_AUTOMATIC, WPD_FOCUS_AUTOMATIC_MACRO, WPD_FOCUS_MANUAL, WPD_FOCUS_MODES, WPD_FOCUS_MODES enumeration [Windows Portable Devices SDK], WPD_FOCUS_UNDEFINED, enumeration [Windows Portable Devices SDK], portabledevice/WPD_FOCUS_AUTOMATIC, portabledevice/WPD_FOCUS_AUTOMATIC_MACRO, portabledevice/WPD_FOCUS_MANUAL, portabledevice/WPD_FOCUS_MODES, portabledevice/WPD_FOCUS_UNDEFINED, tagWPD_FOCUS_MODES, wpdsdk.wpd_focus_modes
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
req.typenames: WPD_FOCUS_MODES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_FOCUS_MODES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_FOCUS_MODES enumeration


## -description



        The<b> WPD_FOCUS_MODES</b> enumeration type describes the focus mode used by a still image capture device.
      


## -enum-fields




### -field WPD_FOCUS_UNDEFINED


            The focus mode has not been specified.
          


### -field WPD_FOCUS_MANUAL


            Specifies manual focus.
          


### -field WPD_FOCUS_AUTOMATIC


            Specifies automatic focus, controlled by the device.
          


### -field WPD_FOCUS_AUTOMATIC_MACRO


            Specifies that the device should automatically switch between macro and normal focus, as required.
          


## -remarks




        This enumeration is used by the <a href="still_image_properties.htm">WPD_STILL_IMAGE_FOCUS_MODE</a> property.
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

