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

# FWPM_NET_EVENT_TYPE_ enumeration


## -description


The <b>FWPM_NET_EVENT_TYPE</b> enumerated type specifies the type of net event.


## -enum-fields




### -field FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE

An IKE/AuthIP main mode failure has occurred.


### -field FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE

An IKE/AuthIP quick mode failure has occurred.


### -field FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE

An AuthIP extended mode failure has occurred.


### -field FWPM_NET_EVENT_TYPE_CLASSIFY_DROP

A drop event has occurred.


### -field FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP

An IPsec kernel drop event has occurred.


### -field FWPM_NET_EVENT_TYPE_IPSEC_DOSP_DROP

An IPsec DoS Protection drop event has occurred.

<div class="alert"><b>Note</b>  Available only in Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>

### -field FWPM_NET_EVENT_TYPE_CLASSIFY_ALLOW

An allow event has occurred.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field FWPM_NET_EVENT_TYPE_CAPABILITY_DROP

An app container network capability drop event has occurred.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field FWPM_NET_EVENT_TYPE_CAPABILITY_ALLOW

An app container network capability allow event has occurred.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field FWPM_NET_EVENT_TYPE_CLASSIFY_DROP_MAC

A MAC layer drop event has occurred.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field FWPM_NET_EVENT_TYPE_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

