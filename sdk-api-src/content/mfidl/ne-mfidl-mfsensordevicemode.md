---
UID: NE:mfidl.__MIDL___MIDL_itf_mfidl_0000_0109_0003
title: MFSensorDeviceMode (mfidl.h)
author: windows-sdk-content
description: Specifies the sharing mode of an IMFSensorDevice.
old-location: mf\mfsensordevicemode.htm
tech.root: medfound
ms.assetid: D405AB48-13EC-4859-91B6-0DB797F85DBE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFSensorDeviceMode, MFSensorDeviceMode enumeration [Media Foundation], MFSensorDeviceMode_Controller, MFSensorDeviceMode_Shared, mf.mfsensordevicemode, mfidl/MFSensorDeviceMode, mfidl/MFSensorDeviceMode_Controller, mfidl/MFSensorDeviceMode_Shared
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFSensorDeviceMode
product: Windows
targetos: Windows
req.typenames: MFSensorDeviceMode
req.redist: 
ms.custom: 19H1
---

# MFSensorDeviceMode enumeration


## -description


Specifies the sharing mode of an <a href="https://msdn.microsoft.com/061EF002-178E-42CA-9D32-7E1282297BA4">IMFSensorDevice</a>.


## -enum-fields




### -field MFSensorDeviceMode_Controller

The device is in controller mode, which means its settings can be modified.


### -field MFSensorDeviceMode_Shared

The device is in shared mode, which means it's settings can't be modified.

