---
UID: NF:xenroll.IEnroll4.getProviderTypeWStr
title: IEnroll4::getProviderTypeWStr (xenroll.h)
description: Retrieves the type of the specified cryptographic service provider (CSP).
helpviewer_keywords: ["IEnroll4 interface [Security]","getProviderTypeWStr method","IEnroll4.getProviderTypeWStr","IEnroll4::getProviderTypeWStr","getProviderTypeWStr","getProviderTypeWStr method [Security]","getProviderTypeWStr method [Security]","IEnroll4 interface","security.ienroll4_getprovidertypewstr","xenroll/IEnroll4::getProviderTypeWStr"]
old-location: security\ienroll4_getprovidertypewstr.htm
tech.root: security
ms.assetid: 64d0d96a-b9d4-4b66-8329-2dfc03ba9ce5
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],getProviderTypeWStr method, IEnroll4.getProviderTypeWStr, IEnroll4::getProviderTypeWStr, getProviderTypeWStr, getProviderTypeWStr method [Security], getProviderTypeWStr method [Security],IEnroll4 interface, security.ienroll4_getprovidertypewstr, xenroll/IEnroll4::getProviderTypeWStr
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
 - IEnroll4::getProviderTypeWStr
 - xenroll/IEnroll4::getProviderTypeWStr
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
 - IEnroll4.getProviderTypeWStr
---

# IEnroll4::getProviderTypeWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>getProviderTypeWStr</b> method retrieves the type of the specified <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).

## -parameters

### -param pwszProvName [in]

A pointer to a null-terminated wide character string that contains the name of the CSP whose type is being requested. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

### -param plProvType [out]

A pointer to a <b>LONG</b> value that receives the CSP type. The CSP type is one of the following values:

<ul>
<li>PROV_RSA_FULL</li>
<li>PROV_RSA_SIG</li>
<li>PROV_DSS</li>
<li>PROV_FORTEZZA</li>
<li>PROV_MS_EXCHANGE</li>
<li>PROV_SSL</li>
<li>PROV_RSA_SCHANNEL</li>
<li>PROV_DSS_DH</li>
<li>PROV_DH_SCHANNEL</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>