---
UID: NF:wincrypt.CertEnumCertificateContextProperties
title: CertEnumCertificateContextProperties function (wincrypt.h)
description: The CertEnumCertificateContextProperties function retrieves the first or next extended property associated with a certificate context.
helpviewer_keywords: ["CertEnumCertificateContextProperties","CertEnumCertificateContextProperties function [Security]","_crypto2_certenumcertificatecontextproperties","security.certenumcertificatecontextproperties","wincrypt/CertEnumCertificateContextProperties"]
old-location: security\certenumcertificatecontextproperties.htm
tech.root: security
ms.assetid: b7304ab2-432b-40c0-8014-7f8874fa36fa
ms.date: 12/05/2018
ms.keywords: CertEnumCertificateContextProperties, CertEnumCertificateContextProperties function [Security], _crypto2_certenumcertificatecontextproperties, security.certenumcertificatecontextproperties, wincrypt/CertEnumCertificateContextProperties
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
 - CertEnumCertificateContextProperties
 - wincrypt/CertEnumCertificateContextProperties
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
 - CertEnumCertificateContextProperties
---

# CertEnumCertificateContextProperties function


## -description

The <b>CertEnumCertificateContextProperties</b> function retrieves the first or next extended property associated with a <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>. Used in a loop, this function can retrieve in sequence all of the extended properties associated with a <i>certificate context</i>.

## -parameters

### -param pCertContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure of the certificate containing the properties to be enumerated.

### -param dwPropId [in]

Property number of the last property enumerated. To get the first property, <i>dwPropId</i> is zero. To retrieve subsequent properties, <i>dwPropId</i> is set to the property number returned by the last call to the function. To enumerate all the properties, function calls continue until the function returns zero. 




Applications can call 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a> with the <i>dwPropId</i> returned by this function to retrieve that property's data.

## -returns

The return value is a <b>DWORD</b> value that identifies a <a href="/windows/desktop/SecGloss/c-gly">certificate context's</a> property. The <b>DWORD</b> value returned by one call of the function can be supplied as the <i>dwPropId</i> in a subsequent call to the function. If there are no more properties to be enumerated or if the function fails, zero is returned.

## -remarks

CERT_KEY_PROV_HANDLE_PROP_ID and CERT_KEY_SPEC_PROP_ID properties are stored as members of the CERT_KEY_CONTEXT_PROP_ID property. They are not enumerated individually.


#### Examples

See 
<a href="/windows/desktop/SecCrypto/example-c-program-listing-the-certificates-in-a-store">Example C Program: Listing the Certificates in a Store</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Extended Property Functions</a>