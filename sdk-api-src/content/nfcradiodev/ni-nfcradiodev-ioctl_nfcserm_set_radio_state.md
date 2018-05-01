---
UID: NI:nfcradiodev.IOCTL_NFCSERM_SET_RADIO_STATE
title: IOCTL_NFCSERM_SET_RADIO_STATE
author: windows-driver-content
description: This IOCTL is used by the SE radio management application or service to query the current radio power state of the proximity device.
old-location: nfpdrivers\ioctl_nfcserm_set_radio_state.htm
old-project: nfpdrivers
ms.assetid: 721AE7FE-927C-4EBA-B33D-C5A5A986951C
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_NFCSERM_SET_RADIO_STATE, IOCTL_NFCSERM_SET_RADIO_STATE control code [Near-Field Proximity Drivers], nfcradiodev/IOCTL_NFCSERM_SET_RADIO_STATE, nfpdrivers.ioctl_nfcserm_set_radio_state
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: nfcradiodev.h
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
req.typenames: INET_FIREWALL_APP_CONTAINER, *PINET_FIREWALL_APP_CONTAINER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nfcradiodev.h
api_name:
-	IOCTL_NFCSERM_SET_RADIO_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_NFCSERM_SET_RADIO_STATE IOCTL


## -description


This IOCTL is used by the SE radio management application or service to query the current radio power state of the proximity device.


## -ioctlparameters




### -input-buffer


<a href="https://msdn.microsoft.com/22FE29AC-790D-40D2-949F-9C132F67AEAB"> NFCRM_SET_RADIO_STATE structure</a>



### -input-buffer-length

sizeof(NFCRM_SET_RADIO_STATE)


### -output-buffer

None


### -output-buffer-length

None


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
<td><b>STATUS_INVALID_DEVICE_STATE</b></td>
<td>This code is returned when the device is already in the proximity radio power state that is being set by the client.</td>
</tr>
<tr>
<td><b>STATUS_INVALID_PARAMETER</b></td>
<td>This code is returned when the output buffer is non-zero.</td>
</tr>
</table>
 

