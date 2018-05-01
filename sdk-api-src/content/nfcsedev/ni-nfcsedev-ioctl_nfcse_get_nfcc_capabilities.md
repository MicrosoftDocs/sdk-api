---
UID: NI:nfcsedev.IOCTL_NFCSE_GET_NFCC_CAPABILITIES
title: IOCTL_NFCSE_GET_NFCC_CAPABILITIES
author: windows-driver-content
description: The IOCTL_NFCSE_GET_NFCC_CAPABILITIES control code returns information about the current NFC controller capabilities, including the maximum Listen Mode Routing table size (defined in section 4.2 of the NFC Controller Interface (NCI) Technical Specification Version 1.1) and supported routing modes.
old-location: nfpdrivers\ioctl_nfcse_get_nfcc_capabilities.htm
old-project: nfpdrivers
ms.assetid: 4323FEDF-A7D0-4B67-BC3D-ECAA7AD1CC08
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_NFCSE_GET_NFCC_CAPABILITIES, IOCTL_NFCSE_GET_NFCC_CAPABILITIES control code [Near-Field Proximity Drivers], _IOCTL_NFCSE_GET_NFCC_CAPABILITIES, nfcsedev/IOCTL_NFCSE_GET_NFCC_CAPABILITIES, nfpdrivers.ioctl_nfcse_get_nfcc_capabilities
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
-	IOCTL_NFCSE_GET_NFCC_CAPABILITIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_NFCSE_GET_NFCC_CAPABILITIES IOCTL


## -description


The <b>IOCTL_NFCSE_GET_NFCC_CAPABILITIES</b> 
   control code returns information about the current NFC controller capabilities, including the  maximum Listen Mode Routing table size (defined in section 4.2 of the <i>NFC Controller Interface (NCI) Technical Specification Version 1.1) </i>and supported routing modes. 


## -ioctlparameters




### -input-buffer

None


### -input-buffer-length

None


### -output-buffer


<a href="https://msdn.microsoft.com/D1F9588B-02D9-49B0-B45F-AF5C140D74E4"> SECURE_ELEMENT_NFCC_CAPABILITIES</a> containing NFC controller capabilities.


### -output-buffer-length

sizeof(SECURE_ELEMENT_NFCC_CAPABILITIES)


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
<td>The buffer supplied was too small for the SECURE_ELEMENT_NFCC_CAPABILITIES structure.</td>
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
 

