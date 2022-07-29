---
UID: NF:certenroll.IX509PrivateKey.put_Existing
title: IX509PrivateKey::put_Existing (certenroll.h)
description: Specifies or retrieves a Boolean value that indicates whether the private key has been created or imported. (Put)
helpviewer_keywords: ["Existing property [Security]","Existing property [Security]","IX509PrivateKey interface","IX509PrivateKey interface [Security]","Existing property","IX509PrivateKey.Existing","IX509PrivateKey.put_Existing","IX509PrivateKey::Existing","IX509PrivateKey::get_Existing","IX509PrivateKey::put_Existing","certenroll/IX509PrivateKey::Existing","certenroll/IX509PrivateKey::get_Existing","certenroll/IX509PrivateKey::put_Existing","put_Existing","security.ix509privatekey_existing_property"]
old-location: security\ix509privatekey_existing_property.htm
tech.root: security
ms.assetid: 0ef32207-1fb0-49a2-95cf-353f907f3fc6
ms.date: 12/05/2018
ms.keywords: Existing property [Security], Existing property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],Existing property, IX509PrivateKey.Existing, IX509PrivateKey.put_Existing, IX509PrivateKey::Existing, IX509PrivateKey::get_Existing, IX509PrivateKey::put_Existing, certenroll/IX509PrivateKey::Existing, certenroll/IX509PrivateKey::get_Existing, certenroll/IX509PrivateKey::put_Existing, put_Existing, security.ix509privatekey_existing_property
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
 - IX509PrivateKey::put_Existing
 - certenroll/IX509PrivateKey::put_Existing
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
 - IX509PrivateKey.Existing
 - IX509PrivateKey.get_Existing
 - IX509PrivateKey.put_Existing
---

# IX509PrivateKey::put_Existing


## -description

The <b>Existing</b> property specifies or retrieves a Boolean value that indicates whether the <a href="/windows/desktop/SecGloss/p-gly">private key</a> has been created or imported. This property is web enabled for both input and output.

This property is read/write.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-create">Create</a> method to create a new private key. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-open">Open</a> method to open an existing key.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
