---
UID: NN:certenroll.IObjectId
title: IObjectId (certenroll.h)
description: Represents an object identifier (OID).
helpviewer_keywords: ["IObjectId","IObjectId interface [Security]","IObjectId interface [Security]","described","certenroll/IObjectId","security.iobjectid"]
old-location: security\iobjectid.htm
tech.root: security
ms.assetid: bc6608e3-cae7-4992-b599-06bc04cc8ad7
ms.date: 12/05/2018
ms.keywords: IObjectId, IObjectId interface [Security], IObjectId interface [Security],described, certenroll/IObjectId, security.iobjectid
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
 - IObjectId
 - certenroll/IObjectId
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
 - IObjectId
---

# IObjectId interface


## -description

The <b>IObjectId</b> interface represents an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). OIDs are returned from numerous Certificate Enrollment API properties, and they  can be used to initialize the following objects:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekey">IX509AttributeArchiveKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionenhancedkeyusage">IX509ExtensionEnhancedKeyUsage</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a>
</li>
</ul>


All of the methods used to initialize an <b>IObjectId</b> object call the CryptoAPI <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a> function which retrieves the first registered <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info">CRYPT_OID_INFO</a> structure that matches the specified parameters. The function searches the registry and static memory on the local computer and Active Directory on the domain server. The  <b>CRYPT_OID_INFO</b> structure is declared in Wincrypt.h and has the following signature.<div class="alert"><b>Note</b>  You cannot use the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info">CRYPT_OID_INFO</a> structure directly in the Certificate Enrollment API.</div>
<div> </div>

## -inheritance

The <b>IObjectId</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IObjectId</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a>
