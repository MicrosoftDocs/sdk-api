---
UID: NF:certenroll.IX509PrivateKey.get_Opened
title: IX509PrivateKey::get_Opened (certenroll.h)
description: Retrieves a Boolean value that specifies whether the private key is open.
helpviewer_keywords: ["IX509PrivateKey interface [Security]","Opened property","IX509PrivateKey.Opened","IX509PrivateKey.get_Opened","IX509PrivateKey::Opened","IX509PrivateKey::get_Opened","Opened property [Security]","Opened property [Security]","IX509PrivateKey interface","certenroll/IX509PrivateKey::Opened","certenroll/IX509PrivateKey::get_Opened","get_Opened","security.ix509privatekey_opened_property"]
old-location: security\ix509privatekey_opened_property.htm
tech.root: security
ms.assetid: 7f02b3d7-ab3a-4413-81ac-c626bc79a88c
ms.date: 12/05/2018
ms.keywords: IX509PrivateKey interface [Security],Opened property, IX509PrivateKey.Opened, IX509PrivateKey.get_Opened, IX509PrivateKey::Opened, IX509PrivateKey::get_Opened, Opened property [Security], Opened property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::Opened, certenroll/IX509PrivateKey::get_Opened, get_Opened, security.ix509privatekey_opened_property
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
 - IX509PrivateKey::get_Opened
 - certenroll/IX509PrivateKey::get_Opened
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
 - IX509PrivateKey.Opened
 - IX509PrivateKey.get_Opened
---

# IX509PrivateKey::get_Opened


## -description

The <b>Opened</b> property retrieves a Boolean value that specifies whether the <a href="/windows/desktop/SecGloss/p-gly">private key</a> is open.

This property is read-only.

## -parameters

## -remarks

You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-create">Create</a> method to create a private key, and call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-open">Open</a> method to open one.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>