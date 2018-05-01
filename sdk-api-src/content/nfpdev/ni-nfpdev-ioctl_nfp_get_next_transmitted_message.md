---
UID: NI:nfpdev.IOCTL_NFP_GET_NEXT_TRANSMITTED_MESSAGE
title: IOCTL_NFP_GET_NEXT_TRANSMITTED_MESSAGE
author: windows-driver-content
description: A client interested in receiving notifications that a message has been transmitted will send the IOCTL_NFP_GET_NEXT_TRANSMITTED_MESSAGE request to the proximity driver.
old-location: nfpdrivers\ioctl_nfp_get_next_transmitted_message.htm
old-project: nfpdrivers
ms.assetid: 3E8B47B5-D774-4D37-BA57-FAB49C9DE9A3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_NFP_GET_NEXT_TRANSMITTED_MESSAGE, IOCTL_NFP_GET_NEXT_TRANSMITTED_MESSAGE control code [Near-Field Proximity Drivers], _IOCTL_NFP_GET_NEXT_TRANSMITTED_MESSAGE, nfpdev/IOCTL_NFP_GET_NEXT_TRANSMITTED_MESSAGE, nfpdrivers.ioctl_nfp_get_next_transmitted_message
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
-	IOCTL_NFP_GET_NEXT_TRANSMITTED_MESSAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_NFP_GET_NEXT_TRANSMITTED_MESSAGE IOCTL


## -description


A client interested in receiving notifications that a message has been transmitted will send the <b>IOCTL_NFP_GET_NEXT_TRANSMITTED_MESSAGE</b> request to the proximity driver.


## -ioctlparameters




### -input-buffer

None


### -input-buffer-length



<text></text>




### -output-buffer

None


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



<ul>
<li>
 A client application will send this IOCTL in a control loop to the publication handle.  Two separate transmissions of the same message would result in triggering two events.

</li>
<li>
The client should send another IOCTL each time the pended one is completed.  The driver MUST use appropriate locks to guarantee that the number of successful completions of this IOCTL equates to the number of times the publication has been transmitted.

</li>
<li>
The following actions are required when using this IOCTL:<ul>
<li>
If this IOCTL is received on a handle that hasn’t previously succeeded an <a href="https://msdn.microsoft.com/library/windows/hardware/jj853321">IOCTL_NFP_SET_PAYLOAD</a>, the driver MUST complete it with STATUS_INVALID_DEVICE_STATE.

</li>
<li>
The driver must maintain the equivalent of a “CompleteEventImmediately” counter (<b>ULONG</b> or larger) in the publication file handle.

</li>
<li>
	When this IOCTL is received in the driver:

<ul>
<li>
If the counter is zero, then the driver MUST pend the IOCTL for later completion.

</li>
<li>
	If the counter is greater than zero, then the driver MUST decrement the counter by one and complete the IOCTL with STATUS_SUCCESS immediately.

</li>
</ul>
</li>
<li>
If the publication is transmitted and no IOCTL is currently pended, the driver MUST increment the “CompleteEventImmediately” counter by one.

</li>
<li>
	If the publication is transmitted while there is a pended IOCTL available, the driver MUST complete the pended IRP with STATUS_SUCCESS and NOT increment the “CompleteEventImmediately” counter.

</li>
<li>
	If the IOCTL contains an input or output buffer the driver MUST complete the IOCTL with STATUS_INVALID_PARAMETER.

</li>
<li>
	If this IOCTL is received while another is currently pended in the publication handle, the second one (or later) MUST be completed with STATUS_INVALID_DEVICE_STATE.

</li>
<li>
The driver MUST support CancelIo of the pended IOCTL.

</li>
</ul>


</li>
</ul>



## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=785320">Near field communication (NFC) overall design guide</a>



<a href="https://msdn.microsoft.com/windows/hardware/drivers/nfc/nfp-design-guide">Near field proximity design guide (Tap and Do, NFP provider model, driver requirements)</a>
 

 

