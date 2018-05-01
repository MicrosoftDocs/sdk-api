---
UID: NI:nfcsedev.IOCTL_NFCSE_SET_ROUTING_TABLE
title: IOCTL_NFCSE_SET_ROUTING_TABLE
author: windows-driver-content
description: Configures NFC controller listen mode routing table.
old-location: nfpdrivers\ioctl_nfcse_set_routing_table.htm
old-project: nfpdrivers
ms.assetid: 54B37EC0-C38A-479C-A45F-424963C4D89A
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_NFCSE_SET_ROUTING_TABLE, IOCTL_NFCSE_SET_ROUTING_TABLE control code [Near-Field Proximity Drivers], nfcsedev/IOCTL_NFCSE_SET_ROUTING_TABLE, nfpdrivers.ioctl_nfcse_set_routing_table
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
-	IOCTL_NFCSE_SET_ROUTING_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_NFCSE_SET_ROUTING_TABLE IOCTL


## -description


Configures NFC controller listen mode routing table. Note that caller has to send complete listen mode routing information in a single call. The caller shall ensure that routing table is less than the cbMaxRoutingTableSize value defined in 4.2.5.1. The total size is computed as per NFC NCI standard sec 6.3.2 and is equal to Number of AID based routes x 4 + sum of cbAid + Number of technology based routes x 5 + Number of protocol based routes x 5. The caller shall ensure that values for technology- and protocol-based routes are conformant to NCI NFC spec sec 6.3.2.




## -ioctlparameters




### -input-buffer


<a href="https://msdn.microsoft.com/AD5E6434-BBBF-44CB-8153-B8F4D4F75E94"> SECURE_ELEMENT_ROUTING_TABLE</a> containing all currently configured routing entries.



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

<b>Irp-&gt;IoStatus.Status</b> is set to <b>STATUS_SUCCESS</b> if the request is successful. Possible error codes are:

<table>
<tr>
<th>Return Code</th>
<th>Description</th>
</tr>
<tr>
<td><b>STATUS_INVALID_BUFFER_SIZE</b></td>
<td>The buffer supplied was greater than NFC controller MAX_ROUTING_TABLE_SIZE.</td>
</tr>
<tr>
<td><b>STATUS_FEATURE_NOT_SUPPORTED</b></td>
<td>  The NFCC does not support listen mode routing configuration.</td>
</tr>
<tr>
<td><b>STATUS_INVALID_PARAMETER</b></td>
<td>This status is returned if the output buffer is non-zero, or values used for technology or protocol is conformant to NFC NCI spec sec 6.3.2, or if duplicate AIDs are used, or when using routing mode that is not supported by current NFC controller capabilities.</td>
</tr>
<tr>
<td><b>STATUS_INVALID_DEVICE_STATE</b></td>
<td>This code is returned if the IOCTL is sent on a handle other than with relative name ‘SEManage’.
</td>
</tr>
</table>
 


## -remarks



The following are requirements that the driver must adhere to.

<ul>
<li>This IOCTL is sent on a handle with a ‘SEManage’ relative file name, otherwise the driver MUST complete it with STATUS_INVALID_DEVICE_STATE.

</li>
<li>The driver shall have initial default listen mode routing table entries that route RF technologies A, B, and F and/or ISO-DEP protocol routed to UICC SE if present. These routing entries may later be overridden by new listen mode routing table configuration initiated by device host.

</li>
<li>The driver shall ensure that protocol NFC-DEP is mapped to device host at all times. Even if the caller doesn’t specify this, the driver needs to add this rule implicitly.

</li>
<li>If this IOCTL is issued when the NFCC is in RF discovery state, the driver needs to put the NFCC into RF idle state, configure the routing table, and restart RF discovery.</li>
</ul>




