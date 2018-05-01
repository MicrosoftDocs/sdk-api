---
UID: NI:nfpdev.IOCTL_NFP_GET_KILO_BYTES_PER_SECOND
title: IOCTL_NFP_GET_KILO_BYTES_PER_SECOND
author: windows-driver-content
description: A client sends the IOCTL_NFP_GET_KILO_BYTES_PER_SECOND request to any generic handle, one that is non-published and non-subscribed, to the provider device.
old-location: nfpdrivers\ioctl_nfp_get_kilo_bytes_per_second.htm
old-project: nfpdrivers
ms.assetid: 7FAF7D15-1D3A-4F90-BD98-344ECF294E0F
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_NFP_GET_KILO_BYTES_PER_SECOND, IOCTL_NFP_GET_KILO_BYTES_PER_SECOND control code [Near-Field Proximity Drivers], _IOCTL_NFP_GET_KILO_BYTES_PER_SECOND, nfpdev/IOCTL_NFP_GET_KILO_BYTES_PER_SECOND, nfpdrivers.ioctl_nfp_get_kilo_bytes_per_second
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
-	IOCTL_NFP_GET_KILO_BYTES_PER_SECOND
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_NFP_GET_KILO_BYTES_PER_SECOND IOCTL


## -description


A client sends the <b>IOCTL_NFP_GET_KILO_BYTES_PER_SECOND</b> request to any generic handle, one that is non-published and non-subscribed, to the provider device. The request is sent in order to determine the approximate best-case transmission speed supported by the provider or its underlying RF technology. This is used to distinguish the difference in one order of magnitude in transmission rate to another.
<div class="alert"><b>Note</b>  A typical NFC implementation should provide a value of approximately 50.</div><div> </div>

## -ioctlparameters




### -input-buffer

None


### -input-buffer-length



<text></text>




### -output-buffer

One <b>INT32</b> value that defines the approximate transmission speed supported by the provider or its underlying technology.


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



Each provider implementation can specify an approximate transmission rate. A typical NFC implementation should provide a value of around 50 KB per second.

The following are required actions when using this IOCTL:<ul>
<li>The driver MUST support an approximate transmission rate no smaller than 16 KB per second.</li>
<li>When this IOCTL is received, the driver MUST copy the approximate transmission speed into the output buffer and complete it with STATUS_SUCCESS.</li>
</ul>





## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=785320">Near field communication (NFC) overall design guide</a>



<a href="https://msdn.microsoft.com/windows/hardware/drivers/nfc/nfp-design-guide">Near field proximity design guide (Tap and Do, NFP provider model, driver requirements)</a>
 

 

