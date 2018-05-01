---
UID: NI:ntddpar.IOCTL_PAR_QUERY_DEVICE_ID
title: IOCTL_PAR_QUERY_DEVICE_ID
author: windows-driver-content
description: The IOCTL_PAR_QUERY_DEVICE_ID request returns the IEEE 1284 device ID of a parallel device assigned by the system-supplied function driver for parallel ports.
old-location: parports\ioctl_par_query_device_id.htm
old-project: parports
ms.assetid: 3f87558a-5c56-46c0-a983-2db2057fcc81
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_PAR_QUERY_DEVICE_ID, IOCTL_PAR_QUERY_DEVICE_ID control code [Parallel Ports], cisspd_29c73c7d-a6fb-4307-b766-ef8b098a1e6f.xml, ntddpar/IOCTL_PAR_QUERY_DEVICE_ID, parports.ioctl_par_query_device_id
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntddpar.h
req.include-header: Ntddpar.h
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
req.typenames: MOUSE_UNIT_ID_PARAMETER, *PMOUSE_UNIT_ID_PARAMETER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntddpar.h
api_name:
-	IOCTL_PAR_QUERY_DEVICE_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_PAR_QUERY_DEVICE_ID IOCTL


## -description



The IOCTL_PAR_QUERY_DEVICE_ID request returns the IEEE 1284 device ID of a parallel device assigned by the system-supplied function driver for parallel ports.




## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

The <b>AssociatedIrp.SystemBuffer</b> member points to a buffer that the client allocates to output the device ID. The buffer contains the device ID and a <b>NULL</b> terminator.


### -output-buffer-length

The <b>Parameters.DeviceIoControl.OutputBufferLength</b> member specifies  the size, in bytes, of the output buffer that can hold both the device ID and a <b>NULL</b> terminator. A client can use an <a href="https://msdn.microsoft.com/library/windows/hardware/ff544080">IOCTL_PAR_QUERY_DEVICE_ID_SIZE</a> request to determine the required buffer size. A device ID can be up to 64 KB in size.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of a buffer that holds both the device ID and a <b>NULL</b> terminator. Otherwise, the <b>Information</b> member is set to zero. 

The <b>Status</b> member is set to one of the generic status values returned by device control requests for parallel devices or to one of the following values:




#### -STATUS_BUFFER_TOO_SMALL

The output buffer that <b>AssociatedIrp.SystemBuffer</b> points to is less than the size, in bytes, of the device ID and a <b>NULL</b> terminator.


#### -STATUS_IO_DEVICE_ERROR

A device I/O error occurred.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544080">IOCTL_PAR_QUERY_DEVICE_ID_SIZE</a>
 

 

