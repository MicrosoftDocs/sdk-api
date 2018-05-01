---
UID: NI:ntddpar.IOCTL_PAR_GET_DEFAULT_MODES
title: IOCTL_PAR_GET_DEFAULT_MODES
author: windows-driver-content
description: The IOCTL_PAR_GET_DEFAULT_MODES request returns the default write (forward) and read (reverse) IEEE 1284 protocols that the system-supplied bus driver for parallel ports uses.
old-location: parports\ioctl_par_get_default_modes.htm
old-project: parports
ms.assetid: d2f440b2-1208-4cae-9790-b93f267499b1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_PAR_GET_DEFAULT_MODES, IOCTL_PAR_GET_DEFAULT_MODES control code [Parallel Ports], cisspd_29dfce16-6dea-4bff-928d-6ab83099595c.xml, ntddpar/IOCTL_PAR_GET_DEFAULT_MODES, parports.ioctl_par_get_default_modes
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
-	IOCTL_PAR_GET_DEFAULT_MODES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_PAR_GET_DEFAULT_MODES IOCTL


## -description



The IOCTL_PAR_GET_DEFAULT_MODES request returns the default write (forward) and read (reverse) IEEE 1284 protocols that the system-supplied bus driver for parallel ports uses. The default write protocol is CENTRONICS; the default read protocol is NIBBLE. 

For more information, see <a href="https://msdn.microsoft.com/2ff53ed0-dbb7-4c8f-b6e4-5f7d20124a7c">Setting and Clearing a Communication Mode for a Parallel Device</a>.




## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

The <b>AssociatedIrp.SystemBuffer</b> member points to a PARCLASS_NEGOTIATION_MASK structure that the client allocates to output mode information. The system-supplied bus driver for parallel ports sets the <b>usReadMask</b> member and the <b>usWriteMask</b> member. The default write mode is CENTRONICS; the default read mode is NIBBLE.


### -output-buffer-length

The value of the <b>Parameters.DeviceIoControl.OutputBufferLength</b> member is set to the size, in bytes, of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff544343">PARCLASS_NEGOTIATION_MASK</a> structure. 


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of a PARCLASS_NEGOTIATION_MASK structure. Otherwise, <b>Information</b> is set to zero. 

The <b>Status</b> member is set to one of the generic status values returned by device control requests for parallel devices or to the following value:




#### -STATUS_BUFFER_TOO_SMALL

The value of the <b>Parameters.DeviceIoControl.OutputBufferLength</b> is less than the size, in bytes, of a PARCLASS_NEGOTIATION_MASK structure.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543975">IOCTL_IEEE1284_GET_MODE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543978">IOCTL_IEEE1284_NEGOTIATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544067">IOCTL_PAR_GET_DEVICE_CAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544343">PARCLASS_NEGOTIATION_MASK</a>
 

 

