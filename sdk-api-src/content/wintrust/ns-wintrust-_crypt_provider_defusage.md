---
UID: NS:wintrust._CRYPT_PROVIDER_DEFUSAGE
title: "_CRYPT_PROVIDER_DEFUSAGE"
author: windows-sdk-content
description: Used by the WintrustGetDefaultForUsage function to retrieve callback information for a provider's default usage.
old-location: security\crypt_provider_defusage.htm
old-project: SecCrypto
ms.assetid: 28A93F39-0CBC-432C-841B-83B54A50EA14
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: "*PCRYPT_PROVIDER_DEFUSAGE, CRYPT_PROVIDER_DEFUSAGE, CRYPT_PROVIDER_DEFUSAGE structure [Security], PCRYPT_PROVIDER_DEFUSAGE, PCRYPT_PROVIDER_DEFUSAGE structure pointer [Security], _CRYPT_PROVIDER_DEFUSAGE, security.crypt_provider_defusage, wintrust/CRYPT_PROVIDER_DEFUSAGE, wintrust/PCRYPT_PROVIDER_DEFUSAGE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CRYPT_PROVIDER_DEFUSAGE, *PCRYPT_PROVIDER_DEFUSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - CRYPT_PROVIDER_DEFUSAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

