---
UID: NF:gamingdeviceinformation.GetGamingDeviceModelInformation
title: GetGamingDeviceModelInformation function (gamingdeviceinformation.h)
description: Gets information about the device that the game is running on.
helpviewer_keywords: ["GetGamingDeviceModelInformation","GetGamingDeviceModelInformation function","gamingdeviceinformation/GetGamingDeviceModelInformation","gamingdvcinfo.getgamingdevicemodelinformation"]
old-location: gamingdvcinfo\getgamingdevicemodelinformation.htm
tech.root: gamingdvcinfo
ms.assetid: 78101CBA-63B5-4B3F-9CEC-A215F32D9EB8
ms.date: 12/05/2018
ms.keywords: GetGamingDeviceModelInformation, GetGamingDeviceModelInformation function, gamingdeviceinformation/GetGamingDeviceModelInformation, gamingdvcinfo.getgamingdevicemodelinformation
req.header: gamingdeviceinformation.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetGamingDeviceModelInformation
 - gamingdeviceinformation/GetGamingDeviceModelInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - api-ms-win-gaming-deviceinformation-l1-1-0.dll
 - gamingdeviceinformation.h
api_name:
 - GetGamingDeviceModelInformation
---

# GetGamingDeviceModelInformation function


## -description

Gets  information about the device that the game is running on.

## -parameters

### -param information [out]

A structure containing information about the device that the game is running on.

## -returns

This function does not return a value.

## -remarks

Supported in both Win32 and UWP apps.

This function gets information about the console that the game is running on, including the type of console (Xbox One, Xbox One S, etc.) and the vendor. On non-Xbox devices, it returns <b>GAMING_DEVICE_DEVICE_ID_NONE</b> and <b>GAMING_DEVICE_VENDOR_ID_NONE</b>.

If the game is running in an emulation mode, the type of device being emulated is returned. For example, if the game is running on an Xbox One X dev kit in Xbox One emulation mode, <b>GAMING_DEVICE_DEVICE_ID_XBOX_ONE</b> is returned.

## -see-also

<a href="/previous-versions/windows/desktop/api/gamingdeviceinformation/ns-gamingdeviceinformation-gaming_device_model_information">GAMING_DEVICE_MODEL_INFORMATION structure</a>



<a href="/previous-versions/windows/desktop/gamingdvcinfo/gaming-device-information-portal">Gaming Device Information</a>