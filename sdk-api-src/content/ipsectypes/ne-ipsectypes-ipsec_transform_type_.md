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

# IPSEC_TRANSFORM_TYPE_ enumeration


## -description



		The <b>IPSEC_TRANSFORM_TYPE</b> enumerated type indicates the type of an IPsec security association (SA) transform.


## -enum-fields




### -field IPSEC_TRANSFORM_AH

Specifies Authentication Header (AH) transform.


### -field IPSEC_TRANSFORM_ESP_AUTH

Specifies Encapsulating Security Payload (ESP)  authentication-only transform.


### -field IPSEC_TRANSFORM_ESP_CIPHER

Specifies ESP cipher transform.


### -field IPSEC_TRANSFORM_ESP_AUTH_AND_CIPHER

Specifies ESP authentication and cipher transform.


### -field IPSEC_TRANSFORM_ESP_AUTH_FW

Specifies that the first packet should be sent twice: once with ESP/AH encapsulation, and once in clear text. The entire session is then sent in clear text.

The initial packet will allow the existing firewall rules to apply to the connection.  The subsequent clear text data stream allows  intermediaries to modify the stream.


<div class="alert"><b>Note</b>  Available only on Windows Server 2008 R2, Windows 7, or later.</div>
<div> </div>



### -field IPSEC_TRANSFORM_TYPE_MAX

Maximum value for testing only.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">WFP Enumerated Types</a>
 

 

