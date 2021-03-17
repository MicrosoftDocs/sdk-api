---
UID: NF:xenroll.IEnroll.enumProvidersWStr
title: IEnroll::enumProvidersWStr (xenroll.h)
description: The IEnroll4::enumProvidersWStr method retrieves the names of the available cryptographic service providers (CSPs) specified by the ProviderType property.
helpviewer_keywords: ["IEnroll interface [Security]","enumProvidersWStr method","IEnroll.enumProvidersWStr","IEnroll::enumProvidersWStr","enumProvidersWStr","enumProvidersWStr method [Security]","enumProvidersWStr method [Security]","IEnroll interface","security.ienroll4_enumproviderswstr","xenroll/IEnroll::enumProvidersWStr"]
old-location: security\ienroll4_enumproviderswstr.htm
tech.root: security
ms.assetid: f3b40f56-3332-44e8-9753-4107948d0801
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],enumProvidersWStr method, IEnroll.enumProvidersWStr, IEnroll::enumProvidersWStr, enumProvidersWStr, enumProvidersWStr method [Security], enumProvidersWStr method [Security],IEnroll interface, security.ienroll4_enumproviderswstr, xenroll/IEnroll::enumProvidersWStr
req.header: xenroll.h
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnroll::enumProvidersWStr
 - xenroll/IEnroll::enumProvidersWStr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.enumProvidersWStr
---

# IEnroll::enumProvidersWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>enumProvidersWStr</b> method retrieves the names of the available <a href="/windows/desktop/SecGloss/c-gly">cryptographic service providers</a> (CSPs) specified by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype">ProviderType</a> property. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

## -parameters

### -param dwIndex [in]

Specifies the ordinal position of the CSP whose name will be retrieved. Specify zero for the first CSP.

### -param dwFlags [in]

Specifies flags that are passed through to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumprovidersa">CryptEnumProviders</a> function. Not currently used; specify zero.

### -param pbstrProvName [out]

A pointer to a <b>LPWSTR</b> variable that receives the name of a CSP with the specified property type.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. The value ERROR_NO_MORE_ITEMS is returned when there are no more CSPs with the property type indicated by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype">ProviderType</a> property.

## -remarks

If the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype">ProviderType</a> property value has not been set, the default value (usually PROV_RSA_FULL) of <b>ProviderType</b> as set in the registry is used.

The <b>enumProvidersWStr</b> method  calls the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumprovidersa">CryptEnumProviders</a> function.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>