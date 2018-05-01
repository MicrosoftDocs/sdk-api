---
UID: NI:ntddpar.IOCTL_PAR_IS_PORT_FREE
title: IOCTL_PAR_IS_PORT_FREE
author: windows-driver-content
description: The IOCTL_PAR_IS_PORT_FREE request determines if a parallel device's parent parallel port is free at the time the system-supplied bus driver for parallel ports processes the request.
old-location: parports\ioctl_par_is_port_free.htm
old-project: parports
ms.assetid: a64db598-b524-43dd-9831-20cb98cf3c29
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_PAR_IS_PORT_FREE, IOCTL_PAR_IS_PORT_FREE control code [Parallel Ports], cisspd_3f8c9a8d-225c-48cc-b504-235c79037f99.xml, ntddpar/IOCTL_PAR_IS_PORT_FREE, parports.ioctl_par_is_port_free
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
-	IOCTL_PAR_IS_PORT_FREE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_PAR_IS_PORT_FREE IOCTL


## -description



The IOCTL_PAR_IS_PORT_FREE request determines if a parallel device's parent parallel port is free at the time the system-supplied bus driver for parallel ports processes the request. This request is provided primarily for user-mode clients.

This request is processed immediately after the I/O manager calls the parallel port bus driver's dispatch routine for device control requests. Note, however, that the status of the parallel port can change between the time that the parallel port bus driver completes the request and the time that control returns to a user-mode client.

Kernel-mode clients can directly determine if a parallel port is free by calling the system-supplied <a href="https://msdn.microsoft.com/library/windows/hardware/ff544550">PPARALLEL_TRY_ALLOCATE_ROUTINE</a> callback.

For more information, see <a href="https://msdn.microsoft.com/dbfa962e-9de8-4a9c-b962-24b53c41f35d">Locking and Unlocking a ParallelPort for Use by a Parallel Device</a>.




## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

The <b>AssociatedIrp.SystemBuffer</b> member points to a BOOLEAN buffer that the client allocates to output the status of the parallel port. If the parallel port is free, the system-supplied function driver for parallel ports sets the buffer to <b>TRUE</b>, otherwise it sets the buffer to <b>FALSE</b>.


### -output-buffer-length

The length of a BOOLEAN.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

The <b>Information</b> member is set to the size, in bytes, of a BOOLEAN.

The <b>Status</b> member is set to one of the generic status values returned by device control requests for parallel devices or to the following value:




#### -STATUS_BUFFER_TOO_SMALL

The <b>Parameters.DeviceIoControl.OutputBufferLength</b> member is less than the size, in bytes, of a BOOLEAN.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544009">IOCTL_INTERNAL_LOCK_PORT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544026">IOCTL_INTERNAL_PARALLEL_PORT_FREE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544550">PPARALLEL_TRY_ALLOCATE_ROUTINE</a>
 

 

