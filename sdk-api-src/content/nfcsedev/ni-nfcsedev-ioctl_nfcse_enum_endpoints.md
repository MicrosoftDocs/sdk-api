---
UID: NI:nfcsedev.IOCTL_NFCSE_ENUM_ENDPOINTS
title: IOCTL_NFCSE_ENUM_ENDPOINTS
author: windows-driver-content
description: Returns information regarding the list of all the secure elements attached to the NFC controller.
old-location: nfpdrivers\ioctl_nfcse_enum_endpoints.htm
old-project: nfpdrivers
ms.assetid: BDE62A2B-423E-4656-91CC-5EBDE50C6BB0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_NFCSE_ENUM_ENDPOINTS, IOCTL_NFCSE_ENUM_ENDPOINTS control code [Near-Field Proximity Drivers], _IOCTL_NFCSE_ENUM_ENDPOINTS, nfcsedev/IOCTL_NFCSE_ENUM_ENDPOINTS, nfpdrivers.ioctl_nfcse_enum_endpoints
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
-	IOCTL_NFCSE_ENUM_ENDPOINTS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_NFCSE_ENUM_ENDPOINTS IOCTL


## -description



 Returns information regarding the list of all the secure elements attached to the NFC controller. Note that the caller must allocate an output buffer large enough to hold information regarding all the secure elements that were enumerated by the driver i.e. Total number of SEs Enumerated x Size of the SE endpoint info otherwise the driver should return a STATUS_BUFFER_OVERFLOW error code to the client with the NumberOfEndpoints field containing the number of secure elements enumerated. The GUID identifying the secure element which maybe used to refer to a particular secure element.




## -ioctlparameters




### -input-buffer

None


### -input-buffer-length

None


### -output-buffer

An <a href="https://msdn.microsoft.com/0F69EE38-C124-47A6-B3CA-31F089657894"> SECURE_ELEMENT_ENDPOINT_LIST</a> for each device enumerated.


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
<td><b>STATUS_INVALID_PARAMETER</b></td>
<td>This code is returned when the output buffer is non-zero.</td>
</tr>
<tr>
<td><b>STATUS_BUFFER_OVERFLOW</b></td>
<td>The buffer supplied was too small to receive the routing table configuration.</td>
</tr>
</table>
 


## -remarks



The following are requirements that the driver must adhere to.

<ul>
<li>In the case of integrated secure element the GUID shall be a unique identifier derived from the serial number and/or other unique identification of the secure element.

</li>
<li>For external secure elements, the GUID maybe a fixed constant and identifies only the “socket” into which the secure element is connected.</li>
<li>For device host secure element, the driver shall enumerate it as a SE end point only if it supports Host Card Emulation. The GUID used for DH maybe a fixed constant defined by the driver.</li>
<li>The caller is required to allocate an output buffer large enough to hold the information about all the secure elements that were enumerated by the driver. The buffer must be equal to the total number of SEs enumerated by the driver multiplied by the size of the SE endpoint information. If the appropriate buffer isn’t allocated, the driver returns a STATUS_BUFFER_OVERFLOW error code to the client with the NumberOfEndpoints field that contains the number of secure elements enumerated.</li>
</ul>




