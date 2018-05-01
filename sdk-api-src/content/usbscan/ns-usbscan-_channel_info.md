---
UID: NS:usbscan._CHANNEL_INFO
title: "_CHANNEL_INFO"
author: windows-driver-content
description: The CHANNEL_INFO structure is used as a parameter to DeviceIoControl, when the specified I/O control code is IOCTL_GET_CHANNEL_ALIGN_RQST.
old-location: image\channel_info.htm
old-project: image
ms.assetid: 1f1cb952-9a63-461f-b70f-4cc41b8d88f8
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PCHANNEL_INFO, CHANNEL_INFO, CHANNEL_INFO structure [Imaging Devices], PCHANNEL_INFO, PCHANNEL_INFO structure pointer [Imaging Devices], _CHANNEL_INFO, image.channel_info, stifnc_f0aea91c-5d41-43e5-bb8b-139bfb7c3198.xml, usbscan/CHANNEL_INFO, usbscan/PCHANNEL_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: usbscan.h
req.include-header: Usbscan.h
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
req.typenames: CHANNEL_INFO, *PCHANNEL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	usbscan.h
api_name:
-	CHANNEL_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _CHANNEL_INFO structure


## -description


The CHANNEL_INFO structure is used as a parameter to <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>, when the specified I/O control code is <a href="https://msdn.microsoft.com/library/windows/hardware/ff542849">IOCTL_GET_CHANNEL_ALIGN_RQST</a>.


## -struct-fields




### -field EventChannelSize

Maximum packet size for the interrupt transfer pipe.


### -field uReadDataAlignment

Maximum packet size for the bulk IN transfer pipe.


### -field uWriteDataAlignment

Maximum packet size for the bulk OUT transfer pipe.

