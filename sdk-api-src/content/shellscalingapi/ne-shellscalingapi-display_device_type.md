---
UID: NE:shellscalingapi.__unnamed_enum_0
title: DISPLAY_DEVICE_TYPE (shellscalingapi.h)
description: Indicates whether the device is a primary or immersive type of display.
helpviewer_keywords: ["DEVICE_IMMERSIVE","DEVICE_PRIMARY","DISPLAY_DEVICE_TYPE","DISPLAY_DEVICE_TYPE enumeration [Windows Shell]","shell.display_device_type","shellscalingapi/DEVICE_IMMERSIVE","shellscalingapi/DEVICE_PRIMARY","shellscalingapi/DISPLAY_DEVICE_TYPE"]
old-location: shell\display_device_type.htm
tech.root: shell
ms.assetid: C8964494-339B-4198-A544-3BBCCFEB9596
ms.date: 12/05/2018
ms.keywords: DEVICE_IMMERSIVE, DEVICE_PRIMARY, DISPLAY_DEVICE_TYPE, DISPLAY_DEVICE_TYPE enumeration [Windows Shell], shell.display_device_type, shellscalingapi/DEVICE_IMMERSIVE, shellscalingapi/DEVICE_PRIMARY, shellscalingapi/DISPLAY_DEVICE_TYPE
req.header: shellscalingapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: DISPLAY_DEVICE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAY_DEVICE_TYPE
 - shellscalingapi/DISPLAY_DEVICE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ShellScalingAPI.h
api_name:
 - DISPLAY_DEVICE_TYPE
---

# DISPLAY_DEVICE_TYPE enumeration


## -description

Indicates whether the device is a primary or immersive type of display.
<div class="alert"><b>Note</b>  The functions that use these enumeration values are no longer supported as of Windows 8.1.</div><div> </div>

## -enum-fields

### -field DEVICE_PRIMARY:0

The device is a primary display device.

### -field DEVICE_IMMERSIVE:1

The device is an immersive display device.

## -see-also

<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-getscalefactorfordevice">GetScaleFactorForDevice</a>



<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangenotifications">RegisterScaleChangeNotifications</a>



<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-revokescalechangenotifications">RevokeScaleChangeNotifications</a>
