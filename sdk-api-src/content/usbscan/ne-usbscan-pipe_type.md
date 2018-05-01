---
UID: NE:usbscan.PIPE_TYPE
title: PIPE_TYPE
author: windows-driver-content
description: The PIPE_TYPE data type is used as input to the DeviceIoControl function, if the I/O control code is IOCTL_CANCEL_IO or IOCTL_RESET_PIPE.
old-location: image\pipe_type.htm
old-project: image
ms.assetid: ae3077a3-01a8-4578-9a26-b8b14ec51a7a
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: ALL_PIPE, EVENT_PIPE, PIPE_TYPE, PIPE_TYPE enumeration [Imaging Devices], READ_DATA_PIPE, WRITE_DATA_PIPE, image.pipe_type, stifnc_dd4122fa-8df4-4190-91ec-248a1e63ab64.xml, usbscan/ALL_PIPE, usbscan/EVENT_PIPE, usbscan/PIPE_TYPE, usbscan/READ_DATA_PIPE, usbscan/WRITE_DATA_PIPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: PIPE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	usbscan.h
api_name:
-	PIPE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# PIPE_TYPE enumeration


## -description


The <b>PIPE_TYPE</b> data type is used as input to the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function, if the I/O control code is <a href="https://msdn.microsoft.com/library/windows/hardware/ff542843">IOCTL_CANCEL_IO</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff542872">IOCTL_RESET_PIPE</a>. An interrupt pipe, a bulk IN pipe, and a bulk OUT pipe are associated with each device handle supplied to <b>DeviceIoControl</b>. The specified PIPE_TYPE value indicates on which of these pipes the operation should be performed, as indicated in the following table. 


## -enum-fields




### -field EVENT_PIPE

The operation should be performed on the interrupt pipe.


### -field READ_DATA_PIPE

The operation should be performed on the bulk IN pipe.


### -field WRITE_DATA_PIPE

The operation should be performed on the bulk OUT pipe.


### -field ALL_PIPE

The operation should be performed on <i>all</i> transfer pipes (not just the pipes associated with the device handle supplied to <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>).

