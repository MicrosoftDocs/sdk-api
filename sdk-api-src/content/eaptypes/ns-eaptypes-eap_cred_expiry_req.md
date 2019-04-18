---
UID: NS:eaptypes._EAP_CRED_EXPIRY_REQ
title: EAP_CRED_EXPIRY_REQ (eaptypes.h)
author: windows-sdk-content
description: Contains both the old and new EAP credentials for credential expiry operations.
old-location: eaphost\eap_cred_expiry_req.htm
tech.root: eaphost
ms.assetid: baa2a580-0bfc-450a-9a96-f32d00127fa4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EAP_CRED_EXPIRY_REQ, EAP_CRED_EXPIRY_REQ structure [EAPHost], EAP_CRED_EXPIRY_RESP, PEAP_CRED_EXPIRY_REQ, PEAP_CRED_EXPIRY_REQ structure pointer [EAPHost], _EAP_CRED_EXPIRY_REQ, eaphost.eap_cred_expiry_req, eaptypes/EAP_CRED_EXPIRY_REQ, eaptypes/PEAP_CRED_EXPIRY_REQ
ms.topic: struct
req.header: eaptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - eaptypes.h
api_name:
 - EAP_CRED_EXPIRY_REQ
product: Windows
targetos: Windows
req.typenames: EAP_CRED_EXPIRY_REQ, EAP_CRED_EXPIRY_RESP
req.redist: 
ms.custom: 19H1
---

# EAP_CRED_EXPIRY_REQ structure


## -description


The <b>EAP_CRED_EXPIRY_REQ</b> structure contains both the old and new EAP credentials for credential expiry operations.


## -struct-fields




### -field curCreds


<a href="https://msdn.microsoft.com/e8a2e934-1ded-4159-8cd8-7aeb75ce743a">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure that contains the old EAP credentials.


### -field newCreds


<a href="https://msdn.microsoft.com/e8a2e934-1ded-4159-8cd8-7aeb75ce743a">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure that contains the new EAP credentials. 


## -remarks



The <b>EAP_CRED_EXPIRY_REQ</b> structure can be employed to support Single-Sign-On (SSO).

The <b>EAP_CRED_EXPIRY_REQ</b> structure is identical to the <a href="https://msdn.microsoft.com/59b7f7d0-58af-4368-b3ea-6f180422a673">EAP_CRED_EXPIRY_RESP</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/77595f36-140d-4d8e-af8e-63e9de0031c4">EAPHost Supplicant Structures</a>



<a href="https://msdn.microsoft.com/59b7f7d0-58af-4368-b3ea-6f180422a673">EAP_CRED_EXPIRY_RESP</a>



<a href="https://msdn.microsoft.com/537a90fc-4dd2-44d4-93da-949f31130ac4">EAP_CRED_REQ</a>



<a href="https://msdn.microsoft.com/714c75d8-71c7-4c3f-802a-a5e4f6ca65c2">EAP_CRED_RESP</a>



<a href="https://msdn.microsoft.com/68141611-4a1c-409e-8ed2-3d21a76640c3">EAP_INTERACTIVE_UI_DATA</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

