---
UID: NF:wincrypt.CertEnumCRLContextProperties
title: CertEnumCRLContextProperties function (wincrypt.h)
description: The CertEnumCRLContextProperties function retrieves the first or next extended property associated with a certificate revocation list (CRL) context.
helpviewer_keywords: ["CertEnumCRLContextProperties","CertEnumCRLContextProperties function [Security]","_crypto2_certenumcrlcontextproperties","security.certenumcrlcontextproperties","wincrypt/CertEnumCRLContextProperties"]
old-location: security\certenumcrlcontextproperties.htm
tech.root: security
ms.assetid: 330808ef-9b39-4bd4-ba0b-9e70ec516f33
ms.date: 12/05/2018
ms.keywords: CertEnumCRLContextProperties, CertEnumCRLContextProperties function [Security], _crypto2_certenumcrlcontextproperties, security.certenumcrlcontextproperties, wincrypt/CertEnumCRLContextProperties
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertEnumCRLContextProperties
 - wincrypt/CertEnumCRLContextProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertEnumCRLContextProperties
---

# CertEnumCRLContextProperties function


## -description

The <b>CertEnumCRLContextProperties</b> function retrieves the first or next extended property associated with a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context. Used in a loop, this function can retrieve in sequence all extended properties associated with a CRL context.

## -parameters

### -param pCrlContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure.

### -param dwPropId [in]

Property number of the last property enumerated. To get the first property, <i>dwPropId</i> is zero. To retrieve subsequent properties, <i>dwPropId</i> is set to the property number returned by the last call to the function. To enumerate all the properties, function calls continue until the function returns zero. 




Applications can call 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcrlcontextproperty">CertGetCRLContextProperty</a> with the <i>dwPropId</i> returned by this function to retrieve that property's data.

## -returns

The return value is a <b>DWORD</b> value that identifies a CRL context's property. The <b>DWORD</b> value returned by one call of the function can be supplied as the <i>dwPropId</i> in a subsequent call to the function. If there are no more properties to be enumerated or if the function fails, zero is returned.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcrlcontextproperty">CertGetCRLContextProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Extended Property Functions</a>