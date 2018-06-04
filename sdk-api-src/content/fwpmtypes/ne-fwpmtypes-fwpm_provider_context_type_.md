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

# FWPM_PROVIDER_CONTEXT_TYPE_ enumeration


## -description



		The <b>FWPM_PROVIDER_CONTEXT_TYPE</b> enumerated type specifies types of provider contexts that may be stored in Base Filtering Engine (BFE).


## -enum-fields




### -field FWPM_IPSEC_KEYING_CONTEXT

Specifies keying context type.


### -field FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT

Specifies IPsec IKE quick mode transport context type.


### -field FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT

Specifies IPsec IKE quick mode tunnel context type.


### -field FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT

Specifies IPsec AuthIP quick mode transport context type.


### -field FWPM_IPSEC_AUTHIP_QM_TUNNEL_CONTEXT

Specifies IPsec Authip quick mode tunnel context type.


### -field FWPM_IPSEC_IKE_MM_CONTEXT

Specifies IKE main mode context type.


### -field FWPM_IPSEC_AUTHIP_MM_CONTEXT

Specifies AuthIP main mode context type.


### -field FWPM_CLASSIFY_OPTIONS_CONTEXT

Specifies classify options context type.


### -field FWPM_GENERAL_CONTEXT

Specifies general context type.


### -field FWPM_IPSEC_IKEV2_QM_TUNNEL_CONTEXT

Specifies IKE v2 quick mode tunnel context type.

<div class="alert"><b>Note</b>  Available only in Windows Server 2008 R2, Windows 7, and later.</div>
<div> </div>

### -field FWPM_IPSEC_IKEV2_MM_CONTEXT

Specifies IKE v2 main mode tunnel context type.

<div class="alert"><b>Note</b>  Available only in Windows Server 2008 R2, Windows 7, and later.</div>
<div> </div>

### -field FWPM_IPSEC_DOSP_CONTEXT

Specifies IPsec DoS Protection context type.

<div class="alert"><b>Note</b>  Available only in Windows Server 2008 R2, Windows 7, and later.</div>
<div> </div>

### -field FWPM_IPSEC_IKEV2_QM_TRANSPORT_CONTEXT

Specifies IKE v2 quick mode transport context type.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows 8.</div>
<div> </div>

### -field FWPM_PROVIDER_CONTEXT_TYPE_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

