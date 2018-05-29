---
UID: NE:ipsectypes.IPSEC_TRANSFORM_TYPE_
title: IPSEC_TRANSFORM_TYPE_
author: windows-sdk-content
description: Indicates the type of an IPsec security association (SA) transform.
old-location: fwp\ipsec_transform_type_enum.htm
old-project: FWP
ms.assetid: 068f17f2-8696-4419-9daa-d8f6486e39a3
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IPSEC_TRANSFORM_AH, IPSEC_TRANSFORM_ESP_AUTH, IPSEC_TRANSFORM_ESP_AUTH_AND_CIPHER, IPSEC_TRANSFORM_ESP_AUTH_FW, IPSEC_TRANSFORM_ESP_CIPHER, IPSEC_TRANSFORM_TYPE, IPSEC_TRANSFORM_TYPE enumeration [Filtering], IPSEC_TRANSFORM_TYPE_, IPSEC_TRANSFORM_TYPE_MAX, fwp.ipsec_transform_type_enum, ipsectypes/IPSEC_TRANSFORM_AH, ipsectypes/IPSEC_TRANSFORM_ESP_AUTH, ipsectypes/IPSEC_TRANSFORM_ESP_AUTH_AND_CIPHER, ipsectypes/IPSEC_TRANSFORM_ESP_AUTH_FW, ipsectypes/IPSEC_TRANSFORM_ESP_CIPHER, ipsectypes/IPSEC_TRANSFORM_TYPE, ipsectypes/IPSEC_TRANSFORM_TYPE_MAX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IPSEC_TRANSFORM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ipsectypes.h
api_name:
-	IPSEC_TRANSFORM_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

