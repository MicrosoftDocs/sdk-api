---
UID: NF:certenroll.IX509PrivateKey.get_DefaultContainer
title: IX509PrivateKey::get_DefaultContainer (certenroll.h)
description: Retrieves a Boolean value that specifies whether the private key represents the default key container.
helpviewer_keywords: ["DefaultContainer property [Security]","DefaultContainer property [Security]","IX509PrivateKey interface","IX509PrivateKey interface [Security]","DefaultContainer property","IX509PrivateKey.DefaultContainer","IX509PrivateKey.get_DefaultContainer","IX509PrivateKey::DefaultContainer","IX509PrivateKey::get_DefaultContainer","certenroll/IX509PrivateKey::DefaultContainer","certenroll/IX509PrivateKey::get_DefaultContainer","get_DefaultContainer","security.ix509privatekey_defaultcontainer_property"]
old-location: security\ix509privatekey_defaultcontainer_property.htm
tech.root: security
ms.assetid: 31998dee-b656-47b8-acb5-246e1a10382a
ms.date: 12/05/2018
ms.keywords: DefaultContainer property [Security], DefaultContainer property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],DefaultContainer property, IX509PrivateKey.DefaultContainer, IX509PrivateKey.get_DefaultContainer, IX509PrivateKey::DefaultContainer, IX509PrivateKey::get_DefaultContainer, certenroll/IX509PrivateKey::DefaultContainer, certenroll/IX509PrivateKey::get_DefaultContainer, get_DefaultContainer, security.ix509privatekey_defaultcontainer_property
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
 - IX509PrivateKey::get_DefaultContainer
 - certenroll/IX509PrivateKey::get_DefaultContainer
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
 - IX509PrivateKey.DefaultContainer
 - IX509PrivateKey.get_DefaultContainer
---

# IX509PrivateKey::get_DefaultContainer


## -description

The <b>DefaultContainer</b> property retrieves a Boolean value that specifies whether the private key represents the default key container.

This property is read-only.

## -parameters

## -remarks

Key containers are identified by name. The name can be specified by the client, or it can be a default value supported by the CSP or KSP. For example, some CSPs use the logon name of the current user as the default container name.

This property value is set when the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-open">Open</a> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-create">Create</a> methods are called.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>