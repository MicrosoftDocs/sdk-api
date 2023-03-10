---
UID: NE:gamingdeviceinformation.GAMING_DEVICE_VENDOR_ID
title: GAMING_DEVICE_VENDOR_ID (gamingdeviceinformation.h)
description: Indicates the vendor of the console that the game is running on.
helpviewer_keywords: ["GAMING_DEVICE_VENDOR_ID","GAMING_DEVICE_VENDOR_ID enumeration","GAMING_DEVICE_VENDOR_ID_MICROSOFT","GAMING_DEVICE_VENDOR_ID_NONE","gamingdeviceinformation/GAMING_DEVICE_VENDOR_ID","gamingdeviceinformation/GAMING_DEVICE_VENDOR_ID_MICROSOFT","gamingdeviceinformation/GAMING_DEVICE_VENDOR_ID_NONE","gamingdvcinfo.gaming_device_vendor_id"]
old-location: gamingdvcinfo\gaming_device_vendor_id.htm
tech.root: gamingdvcinfo
ms.assetid: 0A74E610-9853-4299-A278-41C3B7F47D9C
ms.date: 12/05/2018
ms.keywords: GAMING_DEVICE_VENDOR_ID, GAMING_DEVICE_VENDOR_ID enumeration, GAMING_DEVICE_VENDOR_ID_MICROSOFT, GAMING_DEVICE_VENDOR_ID_NONE, gamingdeviceinformation/GAMING_DEVICE_VENDOR_ID, gamingdeviceinformation/GAMING_DEVICE_VENDOR_ID_MICROSOFT, gamingdeviceinformation/GAMING_DEVICE_VENDOR_ID_NONE, gamingdvcinfo.gaming_device_vendor_id
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
req.typenames: GAMING_DEVICE_VENDOR_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GAMING_DEVICE_VENDOR_ID
 - gamingdeviceinformation/GAMING_DEVICE_VENDOR_ID
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
 - GAMING_DEVICE_VENDOR_ID
---

# GAMING_DEVICE_VENDOR_ID enumeration


## -description

Indicates the vendor of the console that the game is running on.

## -enum-fields

### -field GAMING_DEVICE_VENDOR_ID_NONE:0

The vendor of the device is not known.

### -field GAMING_DEVICE_VENDOR_ID_MICROSOFT:0xC2EC5032

The vendor of the device is Microsoft.

## -remarks

This is a Win32 API that's supported in both Win32 and UWP apps. While it works on any device family, it's only really of value on Xbox devices.

## -see-also

<a href="/previous-versions/windows/desktop/api/gamingdeviceinformation/ns-gamingdeviceinformation-gaming_device_model_information">GAMING_DEVICE_MODEL_INFORMATION structure</a>



<a href="/previous-versions/windows/desktop/gamingdvcinfo/gaming-device-information-portal">Gaming Device Information</a>
