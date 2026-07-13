---
UID: NE:mfidl.__MIDL___MIDL_itf_mfidl_0000_0110_0001
title: MFSensorDeviceType (mfidl.h)
description: Specifies the type of a sensor device. A value from this enumeration is returned by IMFSensorDevice::GetDeviceType.
helpviewer_keywords: ["MFSensorDeviceType","MFSensorDeviceType enumeration [Media Foundation]","MFSensorDeviceType_Device","MFSensorDeviceType_FrameProvider","MFSensorDeviceType_MediaSource","MFSensorDeviceType_Unknown","mf.mfsensordevicetype","mfidl/MFSensorDeviceType","mfidl/MFSensorDeviceType_Device","mfidl/MFSensorDeviceType_FrameProvider","mfidl/MFSensorDeviceType_MediaSource","mfidl/MFSensorDeviceType_Unknown"]
old-location: mf\mfsensordevicetype.htm
tech.root: mf
ms.assetid: 13CC03E6-F0E2-4E69-B94F-4CF1BC7D0C23
ms.date: 12/05/2018
ms.keywords: MFSensorDeviceType, MFSensorDeviceType enumeration [Media Foundation], MFSensorDeviceType_Device, MFSensorDeviceType_FrameProvider, MFSensorDeviceType_MediaSource, MFSensorDeviceType_Unknown, mf.mfsensordevicetype, mfidl/MFSensorDeviceType, mfidl/MFSensorDeviceType_Device, mfidl/MFSensorDeviceType_FrameProvider, mfidl/MFSensorDeviceType_MediaSource, mfidl/MFSensorDeviceType_Unknown
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MFSensorDeviceType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mfidl_0000_0110_0001
 - mfidl/__MIDL___MIDL_itf_mfidl_0000_0110_0001
 - MFSensorDeviceType
 - mfidl/MFSensorDeviceType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFSensorDeviceType
---

# MFSensorDeviceType enumeration


## -description

Specifies the type of a sensor device. A value from this enumeration is returned by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-getdevicetype">IMFSensorDevice::GetDeviceType</a>.

## -enum-fields

### -field MFSensorDeviceType_Unknown:0

The sensor device type is unknown.

### -field MFSensorDeviceType_Device

The sensor device is a physical device. Physical cameras may register as <a href="/previous-versions/ff548567(v=vs.85)">KSCATEGORY_SENSOR_CAMERA</a> or <a href="/previous-versions/ff548567(v=vs.85)">KSCATEGORY_VIDEO_CAMERA</a>  or both.

### -field MFSensorDeviceType_MediaSource

The sensor device is a custom media source.

### -field MFSensorDeviceType_FrameProvider

The sensor device is a legacy frame provider.

### -field MFSensorDeviceType_SensorTransform
