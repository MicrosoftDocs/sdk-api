---
UID: NE:winnt.JOB_OBJECT_NET_RATE_CONTROL_FLAGS
title: JOB_OBJECT_NET_RATE_CONTROL_FLAGS
author: windows-sdk-content
description: Specifies types of scheduling policies for network rate control.
old-location: base\job_object_net_rate_control_flags.htm
tech.root: procthread
ms.assetid: D1AD3722-1A15-4BCA-8F0A-6E32A078959A
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: JOB_OBJECT_NET_RATE_CONTROL_DSCP_TAG, JOB_OBJECT_NET_RATE_CONTROL_ENABLE, JOB_OBJECT_NET_RATE_CONTROL_FLAGS, JOB_OBJECT_NET_RATE_CONTROL_FLAGS enumeration, JOB_OBJECT_NET_RATE_CONTROL_MAX_BANDWITH, JOB_OBJECT_NET_RATE_CONTROL_VALID_FLAGS, base.job_object_net_rate_control_flags, winnt/JOB_OBJECT_NET_RATE_CONTROL_DSCP_TAG, winnt/JOB_OBJECT_NET_RATE_CONTROL_ENABLE, winnt/JOB_OBJECT_NET_RATE_CONTROL_FLAGS, winnt/JOB_OBJECT_NET_RATE_CONTROL_MAX_BANDWITH, winnt/JOB_OBJECT_NET_RATE_CONTROL_VALID_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - JOB_OBJECT_NET_RATE_CONTROL_FLAGS
product: Windows
targetos: Windows
req.typenames: JOB_OBJECT_NET_RATE_CONTROL_FLAGS
req.redist: 
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
 

 

