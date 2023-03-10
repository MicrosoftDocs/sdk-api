---
UID: NF:certenroll.IX509PrivateKey.get_UniqueContainerName
title: IX509PrivateKey::get_UniqueContainerName (certenroll.h)
description: Retrieves a unique name for the key container.
helpviewer_keywords: ["IX509PrivateKey interface [Security]","UniqueContainerName property","IX509PrivateKey.UniqueContainerName","IX509PrivateKey.get_UniqueContainerName","IX509PrivateKey::UniqueContainerName","IX509PrivateKey::get_UniqueContainerName","UniqueContainerName property [Security]","UniqueContainerName property [Security]","IX509PrivateKey interface","certenroll/IX509PrivateKey::UniqueContainerName","certenroll/IX509PrivateKey::get_UniqueContainerName","get_UniqueContainerName","security.ix509privatekey_uniquecontainername_property"]
old-location: security\ix509privatekey_uniquecontainername_property.htm
tech.root: security
ms.assetid: 93da413f-556d-4cda-8628-ce4a2150da19
ms.date: 12/05/2018
ms.keywords: IX509PrivateKey interface [Security],UniqueContainerName property, IX509PrivateKey.UniqueContainerName, IX509PrivateKey.get_UniqueContainerName, IX509PrivateKey::UniqueContainerName, IX509PrivateKey::get_UniqueContainerName, UniqueContainerName property [Security], UniqueContainerName property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::UniqueContainerName, certenroll/IX509PrivateKey::get_UniqueContainerName, get_UniqueContainerName, security.ix509privatekey_uniquecontainername_property
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
 - IX509PrivateKey::get_UniqueContainerName
 - certenroll/IX509PrivateKey::get_UniqueContainerName
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
 - IX509PrivateKey.UniqueContainerName
 - IX509PrivateKey.get_UniqueContainerName
---

# IX509PrivateKey::get_UniqueContainerName


## -description

The <b>UniqueContainerName</b> property retrieves a unique name for the key container.

This property is read-only.

## -parameters

## -remarks

This property retrieves an alternate name that can be used when accessing a key when you believe that the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_containername">ContainerName</a> property value is not unique enough to provide adequate identification. Typically the key container creates the name. For example, the Cryptography API: Next Generation (CNG) key storage provider (KSP) returns the name of the encrypted file that contains the key.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>