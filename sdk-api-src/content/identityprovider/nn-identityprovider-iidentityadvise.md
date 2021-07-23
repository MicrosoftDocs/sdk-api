---
UID: NN:identityprovider.IIdentityAdvise
title: IIdentityAdvise (identityprovider.h)
description: Allows an identity provider to notify a calling application when an identity is updated.
helpviewer_keywords: ["IIdentityAdvise","IIdentityAdvise interface [Security]","IIdentityAdvise interface [Security]","described","identityprovider/IIdentityAdvise","identitystore/IIdentityAdvise","security.iidentityadvise"]
old-location: security\iidentityadvise.htm
tech.root: security
ms.assetid: fa348d46-bcd2-4009-89d6-11e738d4a82b
ms.date: 12/05/2018
ms.keywords: IIdentityAdvise, IIdentityAdvise interface [Security], IIdentityAdvise interface [Security],described, identityprovider/IIdentityAdvise, identitystore/IIdentityAdvise, security.iidentityadvise
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIdentityAdvise
 - identityprovider/IIdentityAdvise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - IdentityProvider.h
 - Identitystore.h
api_name:
 - IIdentityAdvise
---

# IIdentityAdvise interface


## -description

The <b>IIdentityAdvise</b> interface allows an identity provider to notify a calling application when an identity is updated.

## -inheritance

The <b>IIdentityAdvise</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIdentityAdvise</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a>



<a href="/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-advise">IIdentityProvider::Advise</a>
