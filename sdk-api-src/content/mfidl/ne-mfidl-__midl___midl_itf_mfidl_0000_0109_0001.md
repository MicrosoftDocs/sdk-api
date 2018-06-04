---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# __MIDL___MIDL_itf_mfidl_0000_0109_0001 enumeration


## -description


Specifies the type of a sensor device. A value from this enumeration is returned by <a href="https://msdn.microsoft.com/6714B5A8-83F2-44CD-B061-749EA6BFBF20">IMFSensorDevice::GetDeviceType</a>.


## -enum-fields




### -field MFSensorDeviceType_Unknown

The sensor device type is unknown.


### -field MFSensorDeviceType_Device

The sensor device is a physical device. Physical cameras may register as <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff548567(v=vs.85).aspx">KSCATEGORY_SENSOR_CAMERA</a> or <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff548567(v=vs.85).aspx">KSCATEGORY_VIDEO_CAMERA</a>  or both.


### -field MFSensorDeviceType_MediaSource

The sensor device is a custom media source.


### -field MFSensorDeviceType_FrameProvider

The sensor device is a legacy frame provider.


### -field MFSensorDeviceType_SensorTransform



