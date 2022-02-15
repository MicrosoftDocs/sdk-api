---
UID: NN:certenroll.IX509AttributeArchiveKeyHash
title: IX509AttributeArchiveKeyHash (certenroll.h)
description: Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority.
helpviewer_keywords: ["IX509AttributeArchiveKeyHash","IX509AttributeArchiveKeyHash interface [Security]","IX509AttributeArchiveKeyHash interface [Security]","described","certenroll/IX509AttributeArchiveKeyHash","security.ix509attributearchivekeyhash"]
old-location: security\ix509attributearchivekeyhash.htm
tech.root: security
ms.assetid: 52c92629-4c9e-4996-80a2-30e2212b3009
ms.date: 12/05/2018
ms.keywords: IX509AttributeArchiveKeyHash, IX509AttributeArchiveKeyHash interface [Security], IX509AttributeArchiveKeyHash interface [Security],described, certenroll/IX509AttributeArchiveKeyHash, security.ix509attributearchivekeyhash
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
 - IX509AttributeArchiveKeyHash
 - certenroll/IX509AttributeArchiveKeyHash
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
 - IX509AttributeArchiveKeyHash
---

# IX509AttributeArchiveKeyHash interface


## -description

The <b>IX509AttributeArchiveKeyHash</b> interface represents an attribute that contains a SHA-1 <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the encrypted  <a href="/windows/desktop/SecGloss/p-gly">private key</a> to be archived by a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>. The encrypted key is attached as an unauthenticated attribute to the primary signature of a CMC request. The hash of the encrypted key is encoded as an authenticated attribute in a CMC request.

When a certification authority receives the request, it hashes the unsigned encrypted key and compares it to the signed hash sent by the requester. If the hashes match, the key was not tampered with.

## -inheritance

The <b>IX509AttributeArchiveKeyHash</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>. <b>IX509AttributeArchiveKeyHash</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>
