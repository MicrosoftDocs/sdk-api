---
UID: NE:gamingdeviceinformation.GAMING_DEVICE_DEVICE_ID
title: GAMING_DEVICE_DEVICE_ID
author: windows-driver-content
description: Indicates the type of device that the game is running on.
old-location: gamingdvcinfo\gaming_device_device_id.htm
old-project: gamingdvcinfo
ms.assetid: DA196767-940E-47CF-8444-4A2C37E3718B
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GAMING_DEVICE_DEVICE_ID, GAMING_DEVICE_DEVICE_ID enumeration, GAMING_DEVICE_DEVICE_ID_NONE, GAMING_DEVICE_DEVICE_ID_XBOX_ONE, GAMING_DEVICE_DEVICE_ID_XBOX_ONE_S, GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X, GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X_DEVKIT, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_NONE, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE_S, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X_DEVKIT, gamingdvcinfo.gaming_device_device_id
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: GAMING_DEVICE_DEVICE_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	gamingdeviceinformation.h
api_name:
-	GAMING_DEVICE_DEVICE_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxsutility.dll
req.irql: 
req.product: Internet Explorer 5
---

# GAMING_DEVICE_DEVICE_ID enumeration


## -description


Indicates the type of device that the game is running on.


## -enum-fields




### -field GAMING_DEVICE_DEVICE_ID_NONE

The device is not in the Xbox family.


### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE

The device is an Xbox One (original).


### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE_S

The device is an Xbox One S.


### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X

The device is an Xbox One X.


### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X_DEVKIT

The device is an Xbox One X dev kit.


## -remarks



This is a Win32 API that's supported in both Win32 and UWP apps. While it works on any device family, it's only really of value on Xbox devices.




## -see-also




<a href="https://msdn.microsoft.com/0D5A6358-0F82-4414-BD17-BDE22EDBBB15">GAMING_DEVICE_MODEL_INFORMATION structure</a>



<a href="https://msdn.microsoft.com/bf210289-5963-4327-828b-98a0d14b5bfa">Gaming Device Information</a>
 

 

