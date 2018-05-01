---
UID: NI:ntddpar.IOCTL_PAR_QUERY_INFORMATION
title: IOCTL_PAR_QUERY_INFORMATION
author: windows-driver-content
description: The IOCTL_PAR_QUERY_INFORMATION request returns the status of an IEEE 1284 end-of-chain device.
old-location: parports\ioctl_par_query_information.htm
old-project: parports
ms.assetid: 272e7810-1242-4e56-8431-bd7c5908247a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_PAR_QUERY_INFORMATION, IOCTL_PAR_QUERY_INFORMATION control code [Parallel Ports], cisspd_50a28bb8-8015-4b25-9850-9038b1c1789a.xml, ntddpar/IOCTL_PAR_QUERY_INFORMATION, parports.ioctl_par_query_information
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
-	IOCTL_PAR_QUERY_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_PAR_QUERY_INFORMATION IOCTL


## -description



The IOCTL_PAR_QUERY_INFORMATION request returns the status of an IEEE 1284 end-of-chain device.




## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

The <b>AssociatedIrp.SystemBuffer</b> member points to a PAR_QUERY_INFORMATION structure that the client allocates to output status information. The system-supplied bus driver for parallel ports sets the <b>Status</b> member to a bitwise OR of one or more of the following operating conditions:

PARALLEL_BUSY

PARALLEL_NOT_CONNECTED

PARALLEL_OFF_LINE

PARALLEL_PAPER_EMPTY

PARALLEL_POWER_OFF

PARALLEL_SELECTED


### -output-buffer-length

The <b>Parameters.DeviceIoControl.OutputBufferLength</b> member is set to the size, in bytes, of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff544353">PAR_QUERY_INFORMATION</a> structure. 


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of a PAR_QUERY_INFORMATION structure. Otherwise, the <b>Information</b> is set to zero. 

The <b>Status</b> member is set to one of the generic status values returned by device control requests for parallel devices or to the following value:




#### -STATUS_BUFFER_TOO_SMALL

The value of the <b>Parameters.DeviceIoControl.OutputBufferLength</b> member is less than the size, in bytes, of a PAR_QUERY_INFORMATION structure.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544091">IOCTL_PAR_QUERY_LOCATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544353">PAR_QUERY_INFORMATION</a>
 

 

