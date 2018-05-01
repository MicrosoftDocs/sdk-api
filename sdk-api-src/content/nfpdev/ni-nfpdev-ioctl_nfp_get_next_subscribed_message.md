---
UID: NI:nfpdev.IOCTL_NFP_GET_NEXT_SUBSCRIBED_MESSAGE
title: IOCTL_NFP_GET_NEXT_SUBSCRIBED_MESSAGE
author: windows-driver-content
description: The client sends the IOCTL_NFP_GET_NEXT_SUBSCRIBED_MESSAGE request to the subscription handle repeatedly in order to receive subscribed messages as they arrive.
old-location: nfpdrivers\ioctl_nfp_get_next_subscribed_message.htm
old-project: nfpdrivers
ms.assetid: 975C32AE-6A2C-44C8-8F53-4158FDF1B942
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_NFP_GET_NEXT_SUBSCRIBED_MESSAGE, IOCTL_NFP_GET_NEXT_SUBSCRIBED_MESSAGE control code [Near-Field Proximity Drivers], nfpdev/IOCTL_NFP_GET_NEXT_SUBSCRIBED_MESSAGE, nfpdrivers.ioctl_nfp_get_next_subscribed_message
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
-	IOCTL_NFP_GET_NEXT_SUBSCRIBED_MESSAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_NFP_GET_NEXT_SUBSCRIBED_MESSAGE IOCTL


## -description


The client sends the <b>IOCTL_NFP_GET_NEXT_SUBSCRIBED_MESSAGE</b> request to the subscription handle repeatedly in order to receive subscribed messages as they arrive.  Typically, this IOCTL will be pended in the subscription handle until a message matching the subscribed type actually arrives.


## -ioctlparameters




### -input-buffer

None


### -input-buffer-length



<text></text>




### -output-buffer

A valid buffer is required for returning the message data when it arrives.  The first <b>DWORD</b> of this buffer is reserved for a hint to the client for the next size of the buffer to be returned.  This buffer will typically initially be 255 bytes, but the driver can request that the client send a bigger buffer by providing just the hint and completing the IOCTL with STATUS_BUFFER_OVERFLOW.


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
The client should send another IOCTL each time the pended one is completed. The driver MUST use appropriate locks to guarantee that the number of successful completions of this IOCTL equates to the number of successful message receptions for the subscription type.

</li>
<li>
The following are required actions when using this IOCTL:<ul>
<li>
If this IOCTL is received on a handle that wasn’t previously opened in the “Subs\” device namespace, the driver MUST complete it with STATUS_INVALID_DEVICE_STATE.

</li>
<li>
The driver must maintain a “Received” queue of received messages that match the subscription type within the subscription file handle.

</li>
<li>
	When this IOCTL is received in the driver:

<ul>
<li>
If the “Received” queue is empty, then the driver MUST pend the IOCTL for later completion.

</li>
<li>
	If the “Received” queue is non-empty, then the driver MUST dequeue one message buffer, copy the message buffer to the IOCTL’s output buffer, and complete the IOCTL with STATUS_SUCCESS immediately.

</li>
</ul>
</li>
<li>
If a message matching the type is received and no IOCTL is currently pended, the driver MUST add the message buffer to the “Received” queue.

</li>
<li>
	If a message matching the type is received and there is a pended IOCTL available (the “Received” queue is empty), the driver MUST copy the message buffer to the IOCTL’s output buffer and complete the pended IRP with STATUS_SUCCESS. The “Received” queue MUST continue to be empty following completion of the pended IRP.

</li>
<li>
	If the driver completes this IOCTL with STATUS_SUCCESS, the first DWORD [4 bytes] of the output buffer MUST contain a hint for the size of the next client buffer and the IOCTL’s Information field MUST contain the size of this message plus <b>sizeof</b>(DWORD) (4 bytes).

</li>
<li>
	If the IOCTL contains an input buffer the driver MUST complete the IOCTL with STATUS_INVALID_PARAMETER.

</li>
<li>
	If a received message has a zero-length payload the driver SHOULD ignore the message.  This is a performance optimization because Windows WILL drop messages with zero-length payloads.

</li>
<li>
If a received message is too large to be copied into this IOCTL’s buffer, the driver MUST copy the required buffer size into the first 4 bytes of the output buffer, set the IOCTL’s “Information” field to sizeof(DWORD) (“4”), and complete the IOCTL with STATUS_BUFFER_OVERFLOW. The message buffer must be left in the “Received” queue.

</li>
<li>
If this IOCTL is received while another is currently pended in the subscription handle, the second (or later) one MUST be completed with STATUS_INVALID_DEVICE_STATE.

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
 

 

