---
UID: NF:identityprovider.IIdentityProvider.UnAdvise
title: IIdentityProvider::UnAdvise (identityprovider.h)
description: Deletes a connection created by calling the Advise method.
helpviewer_keywords: ["IIdentityProvider interface [Security]","UnAdvise method","IIdentityProvider.UnAdvise","IIdentityProvider::UnAdvise","UnAdvise","UnAdvise method [Security]","UnAdvise method [Security]","IIdentityProvider interface","identityprovider/IIdentityProvider::UnAdvise","security.iidentityprovider_unadvise"]
old-location: security\iidentityprovider_unadvise.htm
tech.root: security
ms.assetid: ba8a12fc-ea4c-45b5-8339-9cbc88c160db
ms.date: 12/05/2018
ms.keywords: IIdentityProvider interface [Security],UnAdvise method, IIdentityProvider.UnAdvise, IIdentityProvider::UnAdvise, UnAdvise, UnAdvise method [Security], UnAdvise method [Security],IIdentityProvider interface, identityprovider/IIdentityProvider::UnAdvise, security.iidentityprovider_unadvise
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identityprovider.idl
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
 - IIdentityProvider::UnAdvise
 - identityprovider/IIdentityProvider::UnAdvise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identityprovider.h
api_name:
 - IIdentityProvider.UnAdvise
---

# IIdentityProvider::UnAdvise


## -description

The <b>UnAdvise</b> method deletes a connection created by calling the <a href="/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-advise">Advise</a> method.

## -parameters

### -param dwCookie [in]

A value that identifies the connection to delete.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-advise">Advise</a>



<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a>