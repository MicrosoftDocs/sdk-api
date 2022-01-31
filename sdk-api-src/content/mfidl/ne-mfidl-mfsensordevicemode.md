---
UID: NE:mfidl.__MIDL___MIDL_itf_mfidl_0000_0110_0003
title: MFSensorDeviceMode (mfidl.h)
description: Specifies the sharing mode of an IMFSensorDevice.
helpviewer_keywords: ["MFSensorDeviceMode","MFSensorDeviceMode enumeration [Media Foundation]","MFSensorDeviceMode_Controller","MFSensorDeviceMode_Shared","mf.mfsensordevicemode","mfidl/MFSensorDeviceMode","mfidl/MFSensorDeviceMode_Controller","mfidl/MFSensorDeviceMode_Shared"]
old-location: mf\mfsensordevicemode.htm
tech.root: mf
ms.assetid: D405AB48-13EC-4859-91B6-0DB797F85DBE
ms.date: 12/05/2018
ms.keywords: MFSensorDeviceMode, MFSensorDeviceMode enumeration [Media Foundation], MFSensorDeviceMode_Controller, MFSensorDeviceMode_Shared, mf.mfsensordevicemode, mfidl/MFSensorDeviceMode, mfidl/MFSensorDeviceMode_Controller, mfidl/MFSensorDeviceMode_Shared
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
req.typenames: MFSensorDeviceMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mfidl_0000_0110_0003
 - mfidl/__MIDL___MIDL_itf_mfidl_0000_0110_0003
 - MFSensorDeviceMode
 - mfidl/MFSensorDeviceMode
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
 - MFSensorDeviceMode
---

# MFSensorDeviceMode enumeration


## -description

Specifies the sharing mode of an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a>.

## -enum-fields

### -field MFSensorDeviceMode_Controller:0

The device is in controller mode, which means its settings can be modified.

### -field MFSensorDeviceMode_Shared

The device is in shared mode, which means its settings can't be modified.
