---
UID: NI:nfcsedev.IOCTL_NFCSE_HCE_REMOTE_RECV
title: IOCTL_NFCSE_HCE_REMOTE_RECV
author: windows-driver-content
description: Either returns the next data buffer available, or if there are no more buffered data, the request shall stay pending until an APDU buffer is available for reading.
old-location: nfpdrivers\ioctl_nfcse_hce_remote_recv.htm
old-project: nfpdrivers
ms.assetid: 398AFAEF-D0A9-4BBE-8884-1854C95AA878
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_NFCSE_HCE_REMOTE_RECV, IOCTL_NFCSE_HCE_REMOTE_RECV control code [Near-Field Proximity Drivers], nfcsedev/IOCTL_NFCSE_HCE_REMOTE_RECV, nfpdrivers.ioctl_nfcse_hce_remote_recv
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: nfcsedev.h
req.include-header: 
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
req.typenames: SECURE_ELEMENT_TYPE, *PSECURE_ELEMENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nfcsedev.h
api_name:
-	IOCTL_NFCSE_HCE_REMOTE_RECV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_NFCSE_HCE_REMOTE_RECV IOCTL


## -description


Either returns the next data buffer available, or if there are no more buffered data, the request shall stay pending until an APDU buffer is available for reading. The data buffer shall then be returned to the caller. Note that the caller must allocate an output buffer large enough to hold the largest APDU that has been received + 4 bytes overhead.


## -ioctlparameters




### -input-buffer

None


### -input-buffer-length

None


### -output-buffer


                A <b>DWORD</b> indicating the size of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn905624">SECURE_ELEMENT_HCE_DATA_PACKET</a> structure plus its payload, immediately followed by the <b>SECURE_ELEMENT_HCE_DATA_PACKET</b> structure itself. 


### -output-buffer-length



<text></text>




### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to <b>STATUS_SUCCESS</b> if the request is successful. Possible error codes are:

<table>
<tr>
<th>Return Code</th>
<th>Description</th>
</tr>
<tr>
<td><b>STATUS_BUFFER_OVERFLOW</b></td>
<td>The buffer supplied was too small to receive the notification, the first DWORD will contain the expected buffer size.</td>
</tr>
<tr>
<td><b>STATUS_INVALID_PARAMETER</b></td>
<td> If the input buffer is non-zero.</td>
</tr>
<tr>
<td><b>STATUS_INVALID_DEVICE_STATE</b></td>
<td>If the IOCTL is sent on a handle other than with the relative name 'SEManage'.</td>
</tr>
</table>
 


## -remarks



The following are requirements that the driver must adhere to.

<ul>
<li>This IOCTL is sent on an existing connection after HCE Activated event is triggered.</li>
<li>The driver must support CancelIo on this pended IOCTL.</li>
<li>The driver must maintain a “Received” queue of the received APDU for the current connection.

</li>
<li>When this IOCTL is received in the driver:<ul>
<li>If the “Received” queue is empty, then the driver MUST pend the IOCTL for later completion.</li>
<li>If the “Received” queue is non-empty, then the driver MUST de-queue one APDU, copy the APDU buffer to the IOCTL’s output buffer, and complete the IOCTL with STATUS_SUCCESS immediately.</li>
</ul>
</li>
<li>If the driver completes this IOCTL with STATUS_SUCCESS, the first DWORD [4 bytes] of the output buffer MUST contain the size of the SECURE_ELEMENT_HCE_DATA_PACKET structure plus its payload.</li>
<li>If a received APDU data is too large to be copied into this IOCTL's output buffer, the driver MUST copy the required buffer size into the first 4 bytes of the output buffer, set the IOCTL's information field to sizeof(DWORD), and complete the IOCTL with STATUS_BUFFER_OVERFLOW. The APDU data must be left in the "Received" queue.</li>
</ul>




