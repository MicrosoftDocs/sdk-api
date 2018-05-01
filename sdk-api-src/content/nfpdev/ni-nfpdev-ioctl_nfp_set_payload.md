---
UID: NI:nfpdev.IOCTL_NFP_SET_PAYLOAD
title: IOCTL_NFP_SET_PAYLOAD
author: windows-driver-content
description: A client application sends message data and confirms publication with the IOCTL_NFP_SET_PAYLOAD request.
old-location: nfpdrivers\ioctl_nfp_set_payload.htm
old-project: nfpdrivers
ms.assetid: FF89A868-1289-4D1D-BFA8-17E65ED7F8C4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_NFP_SET_PAYLOAD, IOCTL_NFP_SET_PAYLOAD control code [Near-Field Proximity Drivers], nfpdev/IOCTL_NFP_SET_PAYLOAD, nfpdrivers.ioctl_nfp_set_payload
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: nfpdev.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
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
req.typenames: SECURE_ELEMENT_TECH_ROUTING_INFO, *PSECURE_ELEMENT_TECH_ROUTING_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nfpdev.h
api_name:
-	IOCTL_NFP_SET_PAYLOAD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_NFP_SET_PAYLOAD IOCTL


## -description


A client application sends message data and confirms publication with the <b>IOCTL_NFP_SET_PAYLOAD</b> request.


## -ioctlparameters




### -input-buffer

The input buffer contains the message data to transmit.


### -input-buffer-length



<text></text>




### -output-buffer

None.


### -output-buffer-length



<text></text>




### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block



Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



The following actions are required when using this IOCTL:<ul>
<li>
If this IOCTL is sent on a handle that hasn’t previously been opened on a “Pubs\...” filename, the driver MUST complete it with STATUS_INVALID_DEVICE_STATE.

</li>
<li>
The message data is write-once.  If this IOCTL succeeds once, any subsequent IOCTL_NFP_SET_PAYLOAD received on the same handle MUST be completed with STATUS_INVALID_DEVICE_STATE.

</li>
<li>
If the IOCTL contains an output buffer, the driver MUST complete the IOCTL with STATUS_INVALID_PARAMETER.

</li>
<li>
If the input buffer is larger than the driver’s maximum message size, the driver MUST complete the IOCTL with STATUS_INVALID_BUFFER_SIZE.

</li>
<li>
If any device becomes proximate after this IOCTL succeeds, and before the handle is closed, then the message data (along with its type) MUST be transmitted only once to the proximate device.

</li>
<li>
If the same (or different) device becomes proximate again before the handle is closed, the message MUST be transmitted once again.

</li>
<li>
If a device is currently proximate when this IOCTL is successfully completed, then the message data (along with its type) MUST be transmitted (only once) to the proximate device.  This applies even if the handle is immediately closed.

</li>
</ul>





## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=785320">Near field communication (NFC) overall design guide</a>



<a href="https://msdn.microsoft.com/windows/hardware/drivers/nfc/nfp-design-guide">Near field proximity design guide (Tap and Do, NFP provider model, driver requirements)</a>
 

 

