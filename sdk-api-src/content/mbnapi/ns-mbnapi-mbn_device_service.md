---
UID: NS:mbnapi.MBN_DEVICE_SERVICE
title: MBN_DEVICE_SERVICE (mbnapi.h)
description: The MBN_DEVICE_SERVICE structure provides information about a Mobile Broadband device service.
helpviewer_keywords: ["MBN_DEVICE_SERVICE","MBN_DEVICE_SERVICE structure [Microsoft Broadband Networks]","PMBN_DEVICE_SERVICE","PMBN_DEVICE_SERVICE structure pointer [Microsoft Broadband Networks]","mbn.mbn_device_service","mbnapi/MBN_DEVICE_SERVICE","mbnapi/PMBN_DEVICE_SERVICE"]
old-location: mbn\mbn_device_service.htm
tech.root: mbn
ms.assetid: 83BB1CC3-2F00-4CB0-AF05-A8309D01942D
ms.date: 12/05/2018
ms.keywords: MBN_DEVICE_SERVICE, MBN_DEVICE_SERVICE structure [Microsoft Broadband Networks], PMBN_DEVICE_SERVICE, PMBN_DEVICE_SERVICE structure pointer [Microsoft Broadband Networks], mbn.mbn_device_service, mbnapi/MBN_DEVICE_SERVICE, mbnapi/PMBN_DEVICE_SERVICE
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MBN_DEVICE_SERVICE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_DEVICE_SERVICE
 - mbnapi/MBN_DEVICE_SERVICE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_DEVICE_SERVICE
---

# MBN_DEVICE_SERVICE structure


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_DEVICE_SERVICE</b> structure provides information about a Mobile Broadband device service

## -struct-fields

### -field deviceServiceID

A string that represents the unique ID of a Mobile Broadband device service. This matches the Device Service UUID reported by the Mobile Broadband device.

### -field dataWriteSupported

if <b>TRUE</b>, this device service supports write on bulk data sessions. Otherwise, <b>FALSE</b>.

### -field dataReadSupported

if <b>TRUE</b>, this device service supports read on bulk data sessions. Otherwise, <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicescontext-enumeratedeviceservices">EnumerateDeviceServices</a>