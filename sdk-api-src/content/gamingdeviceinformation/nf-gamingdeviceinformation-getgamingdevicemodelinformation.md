---
UID: NF:gamingdeviceinformation.GetGamingDeviceModelInformation
title: GetGamingDeviceModelInformation function
author: windows-sdk-content
description: Gets information about the device that the game is running on.
old-location: gamingdvcinfo\getgamingdevicemodelinformation.htm
tech.root: gamingdvcinfo
ms.assetid: 78101CBA-63B5-4B3F-9CEC-A215F32D9EB8
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetGamingDeviceModelInformation, GetGamingDeviceModelInformation function, gamingdeviceinformation/GetGamingDeviceModelInformation, gamingdvcinfo.getgamingdevicemodelinformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - GetGamingDeviceModelInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This is a Win32 API that's supported in both Win32 and UWP apps. While it works on any device family, it's only really of value on Xbox devices.

This function gets information about the console that the game is running on, including the type of console (Xbox One, Xbox One S, etc.) and the vendor. On non-Xbox devices, it returns <b>GAMING_DEVICE_DEVICE_ID_NONE</b> and <b>GAMING_DEVICE_VENDOR_ID_NONE</b>.

If the game is running in an emulation mode, the type of device being emulated is returned. For example, if the game is running on an Xbox One X dev kit in Xbox One emulation mode, <b>GAMING_DEVICE_DEVICE_ID_XBOX_ONE</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/0D5A6358-0F82-4414-BD17-BDE22EDBBB15">GAMING_DEVICE_MODEL_INFORMATION structure</a>



<a href="https://msdn.microsoft.com/bf210289-5963-4327-828b-98a0d14b5bfa">Gaming Device Information</a>
 

 

