---
UID: NI:ntddpar.IOCTL_IEEE1284_NEGOTIATE
title: IOCTL_IEEE1284_NEGOTIATE
author: windows-driver-content
description: The IOCTL_IEEE1284_NEGOTIATE request sets the read and write protocols that are used for a parallel device.
old-location: parports\ioctl_ieee1284_negotiate.htm
old-project: parports
ms.assetid: 893af02d-ba26-4367-b2cc-b35d5baa9473
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_IEEE1284_NEGOTIATE, IOCTL_IEEE1284_NEGOTIATE control code [Parallel Ports], cisspd_7d757685-3a5b-47cf-bba9-e7051956ae78.xml, ntddpar/IOCTL_IEEE1284_NEGOTIATE, parports.ioctl_ieee1284_negotiate
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
-	IOCTL_IEEE1284_NEGOTIATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_IEEE1284_NEGOTIATE IOCTL


## -description



The IOCTL_IEEE1284_NEGOTIATE request sets the read and write protocols that are used for a parallel device. This request requires that the parallel port, to which the parallel device is attached, be locked and the parallel device be selected. The system-supplied bus driver for parallel ports negotiates with the parallel device to determine the fastest modes that are supported by both the host chipset and the parallel device from among the modes that are specified by the client. The parallel port bus driver sets the default read and write modes to the negotiated modes.

For more information, see <a href="https://msdn.microsoft.com/2ff53ed0-dbb7-4c8f-b6e4-5f7d20124a7c">Setting and Clearing a Communication Mode for a Parallel Device</a>.




## -ioctlparameters




### -input-buffer

The <b>AssociatedIrp.SystemBuffer</b> member points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff544343">PARCLASS_NEGOTIATION_MASK</a> structure that the client allocates for the input and output of mode information. The client sets the <b>usReadMask</b> and <b>usWriteMask</b> members.


### -input-buffer-length

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to the size, in bytes, of a PARCLASS_NEGOTIATION_MASK structure. 


### -output-buffer

The <b>AssociatedIrp.SystemBuffer</b> points to the PARCLASS_NEGOTIATION_MASK structure that the system-supplied bus driver for parallel ports uses to output mode information. The parallel port bus driver sets the <b>usReadMask</b> and <b>usWriteMask</b> members to the negotiated modes.


### -output-buffer-length

The length of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff544343">PARCLASS_NEGOTIATION_MASK</a> structure.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If request is successful, the <b>Information</b> member is set to the size, in bytes, of a PARCLASS_NEGOTIATION_MASK structure. Otherwise the <b>Information</b> member is set to zero. 

The <b>Status</b> member is set to one of the generic status values returned by device control requests for parallel devices or to the following value:




#### -STATUS_INVALID_PARAMETER

The value of the <b>Parameters.DeviceIoControl.InputBufferLength</b> member is less than the size, in bytes, of a PARCLASS_NEGOTIATION_MASK.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543975">IOCTL_IEEE1284_GET_MODE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544061">IOCTL_PAR_GET_DEFAULT_MODES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544067">IOCTL_PAR_GET_DEVICE_CAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544343">PARCLASS_NEGOTIATION_MASK</a>
 

 

