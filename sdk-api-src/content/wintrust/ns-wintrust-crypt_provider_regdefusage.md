---
UID: NS:wintrust._CRYPT_PROVIDER_REGDEFUSAGE
title: CRYPT_PROVIDER_REGDEFUSAGE (wintrust.h)
description: Used by the WintrustAddDefaultForUsage function to register callback information about a provider's default usage.
helpviewer_keywords: ["*PCRYPT_PROVIDER_REGDEFUSAGE","CRYPT_PROVIDER_REGDEFUSAGE","CRYPT_PROVIDER_REGDEFUSAGE structure [Security]","PCRYPT_PROVIDER_REGDEFUSAGE","PCRYPT_PROVIDER_REGDEFUSAGE structure pointer [Security]","security.crypt_provider_regdefusage","wintrust/CRYPT_PROVIDER_REGDEFUSAGE","wintrust/PCRYPT_PROVIDER_REGDEFUSAGE"]
old-location: security\crypt_provider_regdefusage.htm
tech.root: security
ms.assetid: A6047CBA-E4BA-4A31-B700-C368CFB57895
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROVIDER_REGDEFUSAGE, CRYPT_PROVIDER_REGDEFUSAGE, CRYPT_PROVIDER_REGDEFUSAGE structure [Security], PCRYPT_PROVIDER_REGDEFUSAGE, PCRYPT_PROVIDER_REGDEFUSAGE structure pointer [Security], security.crypt_provider_regdefusage, wintrust/CRYPT_PROVIDER_REGDEFUSAGE, wintrust/PCRYPT_PROVIDER_REGDEFUSAGE'
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
req.typenames: CRYPT_PROVIDER_REGDEFUSAGE, *PCRYPT_PROVIDER_REGDEFUSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PROVIDER_REGDEFUSAGE
 - wintrust/_CRYPT_PROVIDER_REGDEFUSAGE
 - PCRYPT_PROVIDER_REGDEFUSAGE
 - wintrust/PCRYPT_PROVIDER_REGDEFUSAGE
 - CRYPT_PROVIDER_REGDEFUSAGE
 - wintrust/CRYPT_PROVIDER_REGDEFUSAGE
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
 - CRYPT_PROVIDER_REGDEFUSAGE
---

# CRYPT_PROVIDER_REGDEFUSAGE structure


## -description

The <b>CRYPT_PROVIDER_REGDEFUSAGE</b> structure is used by the <a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustadddefaultforusage">WintrustAddDefaultForUsage</a> function to register callback information about a provider's default usage.

## -struct-fields

### -field cbStruct

Size, in bytes, of this structure.

### -field pgActionID

GUID that specifies the provider's default action.

### -field pwszDllName

Pointer to the name of the provider DLL.

### -field pwszLoadCallbackDataFunctionName

Pointer to the name of the function that loads the callback data to be returned when the <a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustgetdefaultforusage">WintrustGetDefaultForUsage</a> function is called with the <i>dwAction</i> parameter set to <b>DWACTION_ALLOCANDFILL</b>. This information also exists in the <a href="/windows/desktop/api/wintrust/ns-wintrust-wintrust_data">WINTRUST_DATA</a> structure.

### -field pwszFreeCallbackDataFunctionName

Pointer to the name of the function that frees allocated memory when the <a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustgetdefaultforusage">WintrustGetDefaultForUsage</a> function is called with the <i>dwAction</i> parameter set to <b>DWACTION_FREE</b>. This information also exists in the <a href="/windows/desktop/api/wintrust/ns-wintrust-wintrust_data">WINTRUST_DATA</a> structure.

## -see-also

<a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_defusage">CRYPT_PROVIDER_DEFUSAGE</a>



<a href="/windows/desktop/api/wintrust/ns-wintrust-wintrust_data">WINTRUST_DATA</a>



<a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustadddefaultforusage">WintrustAddDefaultForUsage</a>