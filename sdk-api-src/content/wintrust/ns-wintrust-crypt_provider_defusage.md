---
UID: NS:wintrust._CRYPT_PROVIDER_DEFUSAGE
title: CRYPT_PROVIDER_DEFUSAGE (wintrust.h)
description: Used by the WintrustGetDefaultForUsage function to retrieve callback information for a provider's default usage.
helpviewer_keywords: ["*PCRYPT_PROVIDER_DEFUSAGE","CRYPT_PROVIDER_DEFUSAGE","CRYPT_PROVIDER_DEFUSAGE structure [Security]","PCRYPT_PROVIDER_DEFUSAGE","PCRYPT_PROVIDER_DEFUSAGE structure pointer [Security]","security.crypt_provider_defusage","wintrust/CRYPT_PROVIDER_DEFUSAGE","wintrust/PCRYPT_PROVIDER_DEFUSAGE"]
old-location: security\crypt_provider_defusage.htm
tech.root: security
ms.assetid: 28A93F39-0CBC-432C-841B-83B54A50EA14
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROVIDER_DEFUSAGE, CRYPT_PROVIDER_DEFUSAGE, CRYPT_PROVIDER_DEFUSAGE structure [Security], PCRYPT_PROVIDER_DEFUSAGE, PCRYPT_PROVIDER_DEFUSAGE structure pointer [Security], security.crypt_provider_defusage, wintrust/CRYPT_PROVIDER_DEFUSAGE, wintrust/PCRYPT_PROVIDER_DEFUSAGE'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPT_PROVIDER_DEFUSAGE, *PCRYPT_PROVIDER_DEFUSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PROVIDER_DEFUSAGE
 - wintrust/_CRYPT_PROVIDER_DEFUSAGE
 - PCRYPT_PROVIDER_DEFUSAGE
 - wintrust/PCRYPT_PROVIDER_DEFUSAGE
 - CRYPT_PROVIDER_DEFUSAGE
 - wintrust/CRYPT_PROVIDER_DEFUSAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - CRYPT_PROVIDER_DEFUSAGE
---

# CRYPT_PROVIDER_DEFUSAGE structure


## -description

The <b>CRYPT_PROVIDER_DEFUSAGE</b> structure is used by the <a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustgetdefaultforusage">WintrustGetDefaultForUsage</a> function to retrieve callback information for a provider's default usage.

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

<a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_regdefusage">CRYPT_PROVIDER_REGDEFUSAGE</a>



<a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustgetdefaultforusage">WintrustGetDefaultForUsage</a>