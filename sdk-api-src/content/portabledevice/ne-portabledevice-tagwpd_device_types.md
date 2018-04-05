---
UID: NE:portabledevice.tagWPD_DEVICE_TYPES
title: tagWPD_DEVICE_TYPES
author: windows-driver-content
description: The WPD_DEVICE_TYPES enumeration type describes the different Windows Portable Device (WPD) types commonly used to determine the basic classification and visual appearance of a portable device.
old-location: wpdsdk\wpd_device_types.htm
old-project: wpd_sdk
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_DEVICE_TYPES, WPD_DEVICE_TYPES enumeration [Windows Portable Devices SDK], WPD_DEVICE_TYPE_AUDIO_RECORDER, WPD_DEVICE_TYPE_CAMERA, WPD_DEVICE_TYPE_GENERIC, WPD_DEVICE_TYPE_MEDIA_PLAYER, WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER, WPD_DEVICE_TYPE_PHONE, WPD_DEVICE_TYPE_VIDEO, portabledevice/WPD_DEVICE_TYPES, portabledevice/WPD_DEVICE_TYPE_AUDIO_RECORDER, portabledevice/WPD_DEVICE_TYPE_CAMERA, portabledevice/WPD_DEVICE_TYPE_GENERIC, portabledevice/WPD_DEVICE_TYPE_MEDIA_PLAYER, portabledevice/WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER, portabledevice/WPD_DEVICE_TYPE_PHONE, portabledevice/WPD_DEVICE_TYPE_VIDEO, tagWPD_DEVICE_TYPES, wpdsdk.wpd_device_types
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
req.typenames: WPD_DEVICE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_DEVICE_TYPES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_DEVICE_TYPES enumeration


## -description



        The <b>WPD_DEVICE_TYPES</b> enumeration type describes the different Windows Portable Device (WPD) types commonly used to determine the basic classification and visual appearance of a portable device.
      


## -enum-fields




### -field WPD_DEVICE_TYPE_GENERIC


            A generic WPD that includes multifunction devices that do not fall into one of the other <a href="https://msdn.microsoft.com/library/windows/hardware/ff597867">WPD_DEVICE_TYPES</a> enumeration values.
          


### -field WPD_DEVICE_TYPE_CAMERA


            A camera device, such as a digital still camera.
          


### -field WPD_DEVICE_TYPE_MEDIA_PLAYER


            A media player device that supports playing audio, video, or viewing pictures, such as a portable music player or portable media center. Not all of this functionally is classified as a WPD_DEVICE_TYPE_MEDIA_PLAYER. For example, portable music player devices are classified as WPD_DEVICE_TYPE_MEDIA_PLAYER.


### -field WPD_DEVICE_TYPE_PHONE


            A phone device, such as a mobile phone.
          


### -field WPD_DEVICE_TYPE_VIDEO


            A video device.
          


### -field WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER


            A personal information manager device.
          


### -field WPD_DEVICE_TYPE_AUDIO_RECORDER


            An audio recorder device.
          


## -remarks



<b>WPD_DEVICE_TYPES</b> are read using the <a href="https://msdn.microsoft.com/11cd5b2b-e8f8-4ba1-8527-f7a403f399d5">IPortableDeviceManager</a> interface. WPD applications may use these values to determine the generic visual appearance of the device. That is, a camera picture is displayed for camera-like devices, a mobile phone picture is displayed for phone-like devices, and so on.
      

<div class="alert"><b>Note</b>  WPD applications must use the capabilities of the portable device to determine functionally, not the <b>WPD_DEVICE_TYPES</b> value.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

