---
UID: NI:ntddpar.IOCTL_PAR_SET_READ_ADDRESS
title: IOCTL_PAR_SET_READ_ADDRESS
author: windows-driver-content
description: The IOCTL_PAR_SET_READ_ADDRESS request sets an extended capabilities port (ECP) or enhanced parallel port (EPP) read address (channel) for a parallel device.
old-location: parports\ioctl_par_set_read_address.htm
old-project: parports
ms.assetid: d6ea5ac7-d324-4986-bbfb-4decd278acf7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_PAR_SET_READ_ADDRESS, IOCTL_PAR_SET_READ_ADDRESS control code [Parallel Ports], cisspd_91a85f87-e3c1-4ccb-aeab-13a484c75224.xml, ntddpar/IOCTL_PAR_SET_READ_ADDRESS, parports.ioctl_par_set_read_address
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
-	IOCTL_PAR_SET_READ_ADDRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_PAR_SET_READ_ADDRESS IOCTL


## -description



The IOCTL_PAR_SET_READ_ADDRESS request sets an extended capabilities port (ECP) or enhanced parallel port (EPP) read address (channel) for a parallel device.




## -ioctlparameters




### -input-buffer

The <b>AssociatedIrp.SystemBuffer</b> member points to a UCHAR buffer that the client allocates to input a read address. The request sets the buffer to an ECP or EPP read address.


### -input-buffer-length

<b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to the size, in bytes, of a UCHAR. 


### -output-buffer

None.


### -output-buffer-length

None.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

The <b>Information</b> member is set to zero. 

The <b>Status</b> member is set to one of the generic status values returned by device control requests for parallel devices or to the following value:




#### -STATUS_INVALID_PARAMETER

<b>Parameters.DeviceIoControl.InputBufferLength</b> is less than the size, in bytes, of a UCHAR. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544115">IOCTL_PAR_SET_WRITE_ADDRESS</a>
 

 

