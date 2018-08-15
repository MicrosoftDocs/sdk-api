---
UID: NE:dxvahd._DXVAHD_DEVICE_TYPE
title: "_DXVAHD_DEVICE_TYPE"
author: windows-sdk-content
description: Specifies the type of Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\dxvahd_device_type.htm
old-project: medfound
ms.assetid: c472f2c6-214d-4bb0-ba9d-8dd04ff2a646
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DXVAHD_DEVICE_TYPE, DXVAHD_DEVICE_TYPE enumeration [Media Foundation], DXVAHD_DEVICE_TYPE_HARDWARE, DXVAHD_DEVICE_TYPE_OTHER, DXVAHD_DEVICE_TYPE_REFERENCE, DXVAHD_DEVICE_TYPE_SOFTWARE, _DXVAHD_DEVICE_TYPE, dxvahd/DXVAHD_DEVICE_TYPE, dxvahd/DXVAHD_DEVICE_TYPE_HARDWARE, dxvahd/DXVAHD_DEVICE_TYPE_OTHER, dxvahd/DXVAHD_DEVICE_TYPE_REFERENCE, dxvahd/DXVAHD_DEVICE_TYPE_SOFTWARE, mf.dxvahd_device_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxvahd.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DXVAHD_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_DEVICE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVAHD_DEVICE_TYPE enumeration


## -description


Specifies the type of Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -enum-fields




### -field DXVAHD_DEVICE_TYPE_HARDWARE

Hardware device. Video processing is performed in the GPU by the driver.


### -field DXVAHD_DEVICE_TYPE_SOFTWARE

Software device. Video processing is performed in the CPU by a software plug-in.


### -field DXVAHD_DEVICE_TYPE_REFERENCE

Reference device. Video processing is performed in the CPU by a software plug-in.


### -field DXVAHD_DEVICE_TYPE_OTHER

Other. The device is neither a hardware device nor a software plug-in.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

