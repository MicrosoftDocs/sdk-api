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

# _CRYPT_PROVIDER_DEFUSAGE structure


## -description


The <b>CRYPT_PROVIDER_DEFUSAGE</b> structure is used by the <a href="https://msdn.microsoft.com/B2ED5489-792F-4B00-A21E-EE1B1462D1C8">WintrustGetDefaultForUsage</a> function to retrieve callback information for a provider's default usage.


## -struct-fields




### -field cbStruct

Size, in bytes, of the structure.


### -field gActionID

GUID that specifies the provider's default action.


### -field pDefPolicyCallbackData

Pointer to a data buffer used to pass policy-specific data to a policy provider.


### -field pDefSIPClientData

Pointer to a data buffer used to pass subject interface package (SIP) specific data to an SIP provider. 


## -see-also




<a href="https://msdn.microsoft.com/A6047CBA-E4BA-4A31-B700-C368CFB57895">CRYPT_PROVIDER_REGDEFUSAGE</a>



<a href="https://msdn.microsoft.com/B2ED5489-792F-4B00-A21E-EE1B1462D1C8">WintrustGetDefaultForUsage</a>
 

 

