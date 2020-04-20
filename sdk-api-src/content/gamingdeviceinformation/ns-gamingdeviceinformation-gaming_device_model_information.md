---
UID: NS:gamingdeviceinformation.GAMING_DEVICE_MODEL_INFORMATION
title: GAMING_DEVICE_MODEL_INFORMATION (gamingdeviceinformation.h)
description: Contains information about the device that the game is running on.helpviewer_keywords: ["GAMING_DEVICE_MODEL_INFORMATION","GAMING_DEVICE_MODEL_INFORMATION structure","gamingdeviceinformation/GAMING_DEVICE_MODEL_INFORMATION","gamingdvcinfo.gaming_device_model_information"]
old-location: gamingdvcinfo\gaming_device_model_information.htm
tech.root: gamingdvcinfo
ms.assetid: 0D5A6358-0F82-4414-BD17-BDE22EDBBB15
ms.date: 12/05/2018
ms.keywords: GAMING_DEVICE_MODEL_INFORMATION, GAMING_DEVICE_MODEL_INFORMATION structure, gamingdeviceinformation/GAMING_DEVICE_MODEL_INFORMATION, gamingdvcinfo.gaming_device_model_information
f1_keywords:
- gamingdeviceinformation/GAMING_DEVICE_MODEL_INFORMATION
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- gamingdeviceinformation.h
api_name:
- GAMING_DEVICE_MODEL_INFORMATION
targetos: Windows
req.typenames: GAMING_DEVICE_MODEL_INFORMATION
req.redist: 
ms.custom: 19H1
---

# GAMING_DEVICE_MODEL_INFORMATION structure


## -description


Contains information about the device that the game is running on.


## -struct-fields




### -field vendorId

The vendor of the device.


### -field deviceId

The type of device.


## -remarks



This is a Win32 API that's supported in both Win32 and UWP apps. While it works on any device family, it's only really of value on Xbox devices.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gamingdvcinfo/gaming-device-information-portal">Gaming Device Information</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gamingdeviceinformation/nf-gamingdeviceinformation-getgamingdevicemodelinformation">GetGamingDeviceModelInformation function</a>
 

 

