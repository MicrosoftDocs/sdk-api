---
UID: NE:gamingdeviceinformation.GAMING_DEVICE_DEVICE_ID
title: GAMING_DEVICE_DEVICE_ID (gamingdeviceinformation.h)
description: Indicates the type of device that the game is running on.
helpviewer_keywords: ["GAMING_DEVICE_DEVICE_ID","GAMING_DEVICE_DEVICE_ID enumeration","GAMING_DEVICE_DEVICE_ID_NONE","GAMING_DEVICE_DEVICE_ID_XBOX_ONE","GAMING_DEVICE_DEVICE_ID_XBOX_ONE_S","GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X","GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X_DEVKIT","gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID","gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_NONE","gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE","gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE_S","gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X","gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X_DEVKIT","gamingdvcinfo.gaming_device_device_id"]
old-location: gamingdvcinfo\gaming_device_device_id.htm
tech.root: gamingdvcinfo
ms.assetid: DA196767-940E-47CF-8444-4A2C37E3718B
ms.date: 12/05/2018
ms.keywords: GAMING_DEVICE_DEVICE_ID, GAMING_DEVICE_DEVICE_ID enumeration, GAMING_DEVICE_DEVICE_ID_NONE, GAMING_DEVICE_DEVICE_ID_XBOX_ONE, GAMING_DEVICE_DEVICE_ID_XBOX_ONE_S, GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X, GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X_DEVKIT, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_NONE, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE_S, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X, gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X_DEVKIT, gamingdvcinfo.gaming_device_device_id
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
req.typenames: GAMING_DEVICE_DEVICE_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GAMING_DEVICE_DEVICE_ID
 - gamingdeviceinformation/GAMING_DEVICE_DEVICE_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - gamingdeviceinformation.h
api_name:
 - GAMING_DEVICE_DEVICE_ID
---

# GAMING_DEVICE_DEVICE_ID enumeration


## -description

Indicates the type of device that the game is running on.

## -enum-fields

### -field GAMING_DEVICE_DEVICE_ID_NONE:0

The device is not in the Xbox family.

### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE:0x768BAE26

The device is an Xbox One (original).

### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE_S:0x2A7361D9

The device is an Xbox One S.

### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X:0x5AD617C7

The device is an Xbox One X.

### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X_DEVKIT:0x10F7CDE3

The device is an Xbox One X dev kit.

## -remarks

This is a Win32 API that's supported in both Win32 and UWP apps. While it works on any device family, it's only really of value on Xbox devices.

## -see-also

<a href="/previous-versions/windows/desktop/api/gamingdeviceinformation/ns-gamingdeviceinformation-gaming_device_model_information">GAMING_DEVICE_MODEL_INFORMATION structure</a>



<a href="/previous-versions/windows/desktop/gamingdvcinfo/gaming-device-information-portal">Gaming Device Information</a>
