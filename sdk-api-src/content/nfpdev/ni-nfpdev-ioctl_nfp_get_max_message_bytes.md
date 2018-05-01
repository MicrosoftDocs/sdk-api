---
UID: NI:nfpdev.IOCTL_NFP_GET_MAX_MESSAGE_BYTES
title: IOCTL_NFP_GET_MAX_MESSAGE_BYTES
author: windows-driver-content
description: A client sends the IOCTL_NFP_GET_MAX_MESSAGE_BYTES request to any generic handle, one that is non-published and non-subscribed, to the provider device to determine the maximum message size supported.
old-location: nfpdrivers\ioctl_nfp_get_max_message_bytes.htm
old-project: nfpdrivers
ms.assetid: 030E00C0-9F28-4EAC-BEBA-6AB0269ABAD5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_NFP_GET_MAX_MESSAGE_BYTES, IOCTL_NFP_GET_MAX_MESSAGE_BYTES control code [Near-Field Proximity Drivers], _IOCTL_NFP_GET_MAX_MESSAGE_BYTES, nfpdev/IOCTL_NFP_GET_MAX_MESSAGE_BYTES, nfpdrivers.ioctl_nfp_get_max_message_bytes
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
-	IOCTL_NFP_GET_MAX_MESSAGE_BYTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_NFP_GET_MAX_MESSAGE_BYTES IOCTL


## -description


A client sends the <b>IOCTL_NFP_GET_MAX_MESSAGE_BYTES</b> request to any generic handle, one that is non-published and non-subscribed, to the provider device to determine the maximum message size supported.


## -ioctlparameters




### -input-buffer

None


### -input-buffer-length



<text></text>




### -output-buffer

One <b>INT32</b> value that defines the maximum message size supported by the provide.


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
Each provider implementation can specify a maximum message size for publications and subscriptions. Windows requires that this maximum provider-supported message size be no less than 10 KB.

</li>
<li>
The following are required actions when using this ioctl:<ul>
<li>
	The driver MUST support a maximum message size no smaller than 10 KB.

</li>
<li>
When this IOCTL is received, the driver MUST copy the maximum message size into the output buffer and complete it with STATUS_SUCCESS.

</li>
</ul>


</li>
</ul>



## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=785320">Near field communication (NFC) overall design guide</a>



<a href="https://msdn.microsoft.com/windows/hardware/drivers/nfc/nfp-design-guide">Near field proximity design guide (Tap and Do, NFP provider model, driver requirements)</a>
 

 

