---
UID: NN:certenroll.IX509AttributeArchiveKey
title: IX509AttributeArchiveKey (certenroll.h)
description: Represents an attribute that contains an encrypted private key to be archived by a certification authority.
helpviewer_keywords: ["IX509AttributeArchiveKey","IX509AttributeArchiveKey interface [Security]","IX509AttributeArchiveKey interface [Security]","described","certenroll/IX509AttributeArchiveKey","security.ix509attributearchivekey"]
old-location: security\ix509attributearchivekey.htm
tech.root: security
ms.assetid: b42111e9-e39e-4192-9aba-47403fb627dc
ms.date: 12/05/2018
ms.keywords: IX509AttributeArchiveKey, IX509AttributeArchiveKey interface [Security], IX509AttributeArchiveKey interface [Security],described, certenroll/IX509AttributeArchiveKey, security.ix509attributearchivekey
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
 - IX509AttributeArchiveKey
 - certenroll/IX509AttributeArchiveKey
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
 - IX509AttributeArchiveKey
---

# IX509AttributeArchiveKey interface


## -description

The <b>IX509AttributeArchiveKey</b> interface represents an attribute that contains an encrypted  <a href="/windows/desktop/SecGloss/p-gly">private key</a> to be archived by a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>. The key is attached as an unauthenticated attribute to the primary signature of a CMC request. The hash of the encrypted key is encoded as an authenticated attribute in the CMC request. For more information, see the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekeyhash">IX509AttributeArchiveKeyHash</a> interface.

## -inheritance

The <b>IX509AttributeArchiveKey</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>. <b>IX509AttributeArchiveKey</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>
