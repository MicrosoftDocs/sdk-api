---
UID: NI:ntddpar.IOCTL_IEEE1284_GET_MODE
title: IOCTL_IEEE1284_GET_MODE
author: windows-driver-content
description: The IOCTL_IEEE1284_GET_MODE request returns the IEEE 1284 read and write protocols that are currently set for a parallel device.
old-location: parports\ioctl_ieee1284_get_mode.htm
old-project: parports
ms.assetid: d4bf4c05-fd60-4770-830c-1b146eaec967
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_IEEE1284_GET_MODE, IOCTL_IEEE1284_GET_MODE control code [Parallel Ports], cisspd_e421ca10-5fc6-444c-bb92-09f680fca56a.xml, ntddpar/IOCTL_IEEE1284_GET_MODE, parports.ioctl_ieee1284_get_mode
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
-	IOCTL_IEEE1284_GET_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_IEEE1284_GET_MODE IOCTL


## -description



The IOCTL_IEEE1284_GET_MODE request returns the IEEE 1284 read and write protocols that are currently set for a parallel device. This request does not require that the parallel port, to which the parallel device is attached, be locked.

For more information, see <a href="https://msdn.microsoft.com/2ff53ed0-dbb7-4c8f-b6e4-5f7d20124a7c">Setting and Clearing a Communication Mode for a Parallel Device</a>.




## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

The <b>AssociatedIrp.SystemBuffer</b> member points to a PARCLASS_NEGOTIATION_MASK structure that the client allocates to output mode information. The system-supplied bus driver for parallel ports specifies the read (reverse) protocol in the <b>usReadMask</b> member and the write (forward) protocol in the <b>usWriteMask </b>member.


### -output-buffer-length

The <b>Parameters.DeviceIoControl.OutputBufferLength</b> member is set to the size, in bytes, of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff544343">PARCLASS_NEGOTIATION_MASK</a> structure. 


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of a PARCLASS_NEGOTIATION_MASK. Otherwise, the <b>Information</b> member is set to zero. 

The <b>Status</b> member is set to one of the generic status values returned by device control requests for parallel devices or to the following value:




#### -STATUS_BUFFER_TOO_SMALL

The value of <b>Parameters.DeviceIoControl.OutputBufferLength</b> is less than the size, in bytes, of a PARCLASS_NEGOTIATION_MASK structure.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543978">IOCTL_IEEE1284_NEGOTIATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544061">IOCTL_PAR_GET_DEFAULT_MODES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544067">IOCTL_PAR_GET_DEVICE_CAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544343">PARCLASS_NEGOTIATION_MASK</a>
 

 

