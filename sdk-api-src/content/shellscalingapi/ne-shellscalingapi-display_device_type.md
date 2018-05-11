---
UID: NE:shellscalingapi.DISPLAY_DEVICE_TYPE
title: DISPLAY_DEVICE_TYPE
author: windows-driver-content
description: Indicates whether the device is a primary or immersive type of display.
old-location: shell\display_device_type.htm
old-project: shell
ms.assetid: C8964494-339B-4198-A544-3BBCCFEB9596
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DEVICE_IMMERSIVE, DEVICE_PRIMARY, DISPLAY_DEVICE_TYPE, DISPLAY_DEVICE_TYPE enumeration [Windows Shell], shell.display_device_type, shellscalingapi/DEVICE_IMMERSIVE, shellscalingapi/DEVICE_PRIMARY, shellscalingapi/DISPLAY_DEVICE_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: DISPLAY_DEVICE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ShellScalingAPI.h
api_name:
-	DISPLAY_DEVICE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# DISPLAY_DEVICE_TYPE enumeration


## -description


Indicates whether the device is a primary or immersive type of display.
<div class="alert"><b>Note</b>  The functions that use these enumeration values are no longer supported as of Windows 8.1.</div><div> </div>

## -enum-fields




### -field DEVICE_PRIMARY

The device is a primary display device.


### -field DEVICE_IMMERSIVE

The device is an immersive display device.


## -see-also




<a href="https://msdn.microsoft.com/5F312914-03F6-42E0-80F9-761D854A81A3">GetScaleFactorForDevice</a>



<a href="https://msdn.microsoft.com/79FB0A54-EBF0-4aab-B631-B4D3EA54D20B">RegisterScaleChangeNotifications</a>



<a href="https://msdn.microsoft.com/95F1D147-D364-4b11-AE2B-CD1FCEA07B5D">RevokeScaleChangeNotifications</a>
 

 

