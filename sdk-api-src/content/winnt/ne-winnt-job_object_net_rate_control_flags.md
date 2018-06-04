---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# JOB_OBJECT_NET_RATE_CONTROL_FLAGS enumeration


## -description


Specifies types of scheduling policies for network rate control.


## -enum-fields




### -field JOB_OBJECT_NET_RATE_CONTROL_ENABLE

Turns on the control of the network traffic. You must set this value if you also set either <b>JOB_OBJECT_NET_RATE_CONTROL_MAX_BANDWIDTH</b> or <b>JOB_OBJECT_NET_RATE_CONTROL_DSCP_TAG</b>.


### -field JOB_OBJECT_NET_RATE_CONTROL_MAX_BANDWIDTH


### -field JOB_OBJECT_NET_RATE_CONTROL_DSCP_TAG

Sets the DSCP field in the packet header to the value of the <b>DscpTag</b> member of the <a href="https://msdn.microsoft.com/CE55BC2A-B27C-490A-9D5A-C18FEC09638C">JOBOBJECT_NET_RATE_CONTROL_INFORMATION</a> structure. For information about DSCP, see <a href="https://msdn.microsoft.com/0b4afa74-0198-482d-af72-9ddf135a8e2f">Differentiated Services</a>.


### -field JOB_OBJECT_NET_RATE_CONTROL_VALID_FLAGS

The combination of all of the valid flags for the <a href="https://msdn.microsoft.com/D1AD3722-1A15-4BCA-8F0A-6E32A078959A">JOB_OBJECT_NET_RATE_CONTROL_FLAGS</a> enumeration.


#### - JOB_OBJECT_NET_RATE_CONTROL_MAX_BANDWITH

Uses the value of the <b>MaxBandwidth</b> member of the <a href="https://msdn.microsoft.com/CE55BC2A-B27C-490A-9D5A-C18FEC09638C">JOBOBJECT_NET_RATE_CONTROL_INFORMATION</a> structure to set the maximum bandwidth for outgoing network traffic for the job, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/CE55BC2A-B27C-490A-9D5A-C18FEC09638C">JOBOBJECT_NET_RATE_CONTROL_INFORMATION</a>
 

 

