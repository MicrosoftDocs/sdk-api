---
UID: NF:certenroll.IX509PrivateKey.get_ProviderType
title: IX509PrivateKey::get_ProviderType (certenroll.h)
description: Specifies or retrieves the type of cryptographic provider associated with the private key. (Get)
helpviewer_keywords: ["IX509PrivateKey interface [Security]","ProviderType property","IX509PrivateKey.ProviderType","IX509PrivateKey.get_ProviderType","IX509PrivateKey::ProviderType","IX509PrivateKey::get_ProviderType","IX509PrivateKey::put_ProviderType","ProviderType property [Security]","ProviderType property [Security]","IX509PrivateKey interface","certenroll/IX509PrivateKey::ProviderType","certenroll/IX509PrivateKey::get_ProviderType","certenroll/IX509PrivateKey::put_ProviderType","get_ProviderType","security.ix509privatekey_providertype"]
old-location: security\ix509privatekey_providertype.htm
tech.root: security
ms.assetid: 5f4d2e29-8c02-4d9c-a3a6-15c222650c3e
ms.date: 12/05/2018
ms.keywords: IX509PrivateKey interface [Security],ProviderType property, IX509PrivateKey.ProviderType, IX509PrivateKey.get_ProviderType, IX509PrivateKey::ProviderType, IX509PrivateKey::get_ProviderType, IX509PrivateKey::put_ProviderType, ProviderType property [Security], ProviderType property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::ProviderType, certenroll/IX509PrivateKey::get_ProviderType, certenroll/IX509PrivateKey::put_ProviderType, get_ProviderType, security.ix509privatekey_providertype
req.header: certenroll.h
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509PrivateKey::get_ProviderType
 - certenroll/IX509PrivateKey::get_ProviderType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PrivateKey.ProviderType
 - IX509PrivateKey.get_ProviderType
 - IX509PrivateKey.put_ProviderType
---

# IX509PrivateKey::get_ProviderType


## -description

The <b>ProviderType</b> property specifies or retrieves the type of cryptographic provider associated with the <a href="/windows/desktop/SecGloss/p-gly">private key</a>. This property is web enabled for both input and output.

This property is read/write.

## -parameters

## -remarks

You can use this property to force the use of the default provider for a given provider type. For example, to use the <b>PROV_RSA_SCHANNEL</b> provider, set this property to the <b>XCN_PROV_RSA_SCHANNEL</b><a href="/windows/desktop/api/certenroll/ne-certenroll-x509providertype">X509ProviderType</a> enumeration value and do not specify a value for the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_providername">ProviderName</a> property.

Setting this property automatically sets the following properties to be consistent with the specified <b>ProviderType</b> value:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyspec">KeySpec</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_legacycsp">LegacyCsp</a>
</li>
</ul>
These properties are set in the following manner:

<ul>
<li>If the <b>ProviderType</b> is set to <b>XCN_PROV_NONE</b>:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_legacycsp">LegacyCsp</a> property is set to <b>VARIANT_FALSE</b>.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyspec">KeySpec</a> property is set to <b>XCN_AT_NONE</b>.</li>
</ul>
</li>
<li>If the <b>ProviderType</b> is not set to <b>XCN_PROV_NONE</b>:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_legacycsp">LegacyCsp</a> property is set to <b>VARIANT_TRUE</b>.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyspec">KeySpec</a> property is set to <b>XCN_AT_SIGNATURE</b> if the  current value is <b>XCN_AT_NONE</b>.</li>
</ul>
</li>
</ul>
Because  a previously specified <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_providername">ProviderName</a> is not affected by setting the <b>ProviderType</b> property, setting a <b>ProviderType</b> that is inconsistent with the <b>ProviderName</b> property will result in undefined behavior, likely a failure when creating or opening a private key. We recommend that you set the <b>ProviderType</b> property only when attempting to force the use of the default provider for the specified type as discussed above.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
