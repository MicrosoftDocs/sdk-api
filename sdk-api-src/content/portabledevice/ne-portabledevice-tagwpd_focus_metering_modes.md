---
UID: NE:portabledevice.tagWPD_FOCUS_METERING_MODES
title: tagWPD_FOCUS_METERING_MODES
author: windows-driver-content
description: The WPD_FOCUS_METERING_MODES enumeration type describes how a device should decide what part of a frame to use to set focus.
old-location: wpdsdk\wpd_focus_metering_modes.htm
old-project: wpd_sdk
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_FOCUS_METERING_MODES, WPD_FOCUS_METERING_MODES enumeration [Windows Portable Devices SDK], WPD_FOCUS_METERING_MODE_CENTER_SPOT, WPD_FOCUS_METERING_MODE_MULTI_SPOT, WPD_FOCUS_METERING_MODE_UNDEFINED, enumeration [Windows Portable Devices SDK], portabledevice/WPD_FOCUS_METERING_MODES, portabledevice/WPD_FOCUS_METERING_MODE_CENTER_SPOT, portabledevice/WPD_FOCUS_METERING_MODE_MULTI_SPOT, portabledevice/WPD_FOCUS_METERING_MODE_UNDEFINED, tagWPD_FOCUS_METERING_MODES, wpdsdk.wpd_focus_metering_modes
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
req.typenames: WPD_FOCUS_METERING_MODES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_FOCUS_METERING_MODES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_FOCUS_METERING_MODES enumeration


## -description



        The <b>WPD_FOCUS_METERING_MODES</b> enumeration type describes how a device should decide what part of a frame to use to set focus.
      


## -enum-fields




### -field WPD_FOCUS_METERING_MODE_UNDEFINED


            Indicates that no focusing mode has been specified.
          


### -field WPD_FOCUS_METERING_MODE_CENTER_SPOT


            Focuses on the center of the framed area.
          


### -field WPD_FOCUS_METERING_MODE_MULTI_SPOT


            Determine focus by analyzing multiple parts of the framed area.
          


## -remarks




        This enumeration is specified by the <a href="still_image_properties.htm">WPD_STILL_IMAGE_FOCUS_METERING_MODE</a> property.
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

