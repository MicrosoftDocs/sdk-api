---
UID: NI:ntddpar.IOCTL_PAR_SET_INFORMATION
title: IOCTL_PAR_SET_INFORMATION
author: windows-driver-content
description: The IOCTL_PAR_SET_INFORMATION request resets and initializes a parallel device.
old-location: parports\ioctl_par_set_information.htm
old-project: parports
ms.assetid: a54902d0-aa07-4cd0-8ef1-a3c17dff2ac9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_PAR_SET_INFORMATION, IOCTL_PAR_SET_INFORMATION control code [Parallel Ports], cisspd_950d6397-7eff-4966-a734-0497f1a84257.xml, ntddpar/IOCTL_PAR_SET_INFORMATION, parports.ioctl_par_set_information
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
-	IOCTL_PAR_SET_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_PAR_SET_INFORMATION IOCTL


## -description



The IOCTL_PAR_SET_INFORMATION request resets and initializes a parallel device.




## -ioctlparameters




### -input-buffer

The <b>AssociatedIrp.SystemBuffer</b> member points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff544360">PAR_SET_INFORMATION</a> structure that the client allocates to input set information. The client sets the <b>Init</b> member to PARALLEL_INIT.


### -input-buffer-length

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to the size, in bytes, of a PAR_SET_INFORMATION structure. 


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

The <b>Status</b> member is set to one of the generic status values returned by device control requests for parallel devices or to one of the following values:




#### -STATUS_BUFFER_TOO_SMALL

<b>Parameters.DeviceIoControl.InputBufferLength</b> is less than the size, in bytes, of a PAR_SET_INFORMATION structure. 


#### -STATUS_DEVICE_NOT_CONNECTED

The device is not connected.


#### -STATUS_DEVICE_OFF_LINE

The device is offline.


#### -STATUS_DEVICE_PAPER_EMPTY

The device is out of paper.


#### -STATUS_DEVICE_POWERED_OFF

The device is not turned on.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544086">IOCTL_PAR_QUERY_INFORMATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544360">PAR_SET_INFORMATION</a>
 

 

