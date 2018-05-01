---
UID: NS:usbscan._USBSCAN_PIPE_CONFIGURATION
title: "_USBSCAN_PIPE_CONFIGURATION"
author: windows-driver-content
description: The USBSCAN_PIPE_CONFIGURATION structure is used as a parameter to DeviceIoControl, when the specified I/O control code is IOCTL_GET_PIPE_CONFIGURATION.
old-location: image\usbscan_pipe_configuration.htm
old-project: image
ms.assetid: c9b0247b-1444-46c9-a430-897594f8d223
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PUSBSCAN_PIPE_CONFIGURATION, PUSBSCAN_PIPE_CONFIGURATION, PUSBSCAN_PIPE_CONFIGURATION structure pointer [Imaging Devices], USBSCAN_PIPE_CONFIGURATION, USBSCAN_PIPE_CONFIGURATION structure [Imaging Devices], _USBSCAN_PIPE_CONFIGURATION, image.usbscan_pipe_configuration, stifnc_b18d3edd-f392-4b68-82e4-10f870c18f6a.xml, usbscan/PUSBSCAN_PIPE_CONFIGURATION, usbscan/USBSCAN_PIPE_CONFIGURATION"
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
req.typenames: USBSCAN_PIPE_CONFIGURATION, *PUSBSCAN_PIPE_CONFIGURATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	usbscan.h
api_name:
-	USBSCAN_PIPE_CONFIGURATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _USBSCAN_PIPE_CONFIGURATION structure


## -description


The USBSCAN_PIPE_CONFIGURATION structure is used as a parameter to <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>, when the specified I/O control code is <a href="https://msdn.microsoft.com/library/windows/hardware/ff542859">IOCTL_GET_PIPE_CONFIGURATION</a>.


## -struct-fields




### -field NumberOfPipes

The number of transfer pipes supported for the device.


### -field PipeInfo

Pointer to a <b>NumberOfPipes</b>-sized array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff548547">USBSCAN_PIPE_INFORMATION</a> structures.

