---
UID: NF:identitystore.IIdentityStore.GetCount
title: IIdentityStore::GetCount (identitystore.h)
description: Gets the number of identity providers registered on the system.
helpviewer_keywords: ["GetCount","GetCount method [Security]","GetCount method [Security]","IIdentityStore interface","IIdentityStore interface [Security]","GetCount method","IIdentityStore.GetCount","IIdentityStore::GetCount","identitystore/IIdentityStore::GetCount","security.iidentitystore_getcount"]
old-location: security\iidentitystore_getcount.htm
tech.root: security
ms.assetid: f7f30ab9-f55d-44fa-9098-c6bf865125f8
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Security], GetCount method [Security],IIdentityStore interface, IIdentityStore interface [Security],GetCount method, IIdentityStore.GetCount, IIdentityStore::GetCount, identitystore/IIdentityStore::GetCount, security.iidentitystore_getcount
req.header: identitystore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identitystore.idl
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
 - IIdentityStore::GetCount
 - identitystore/IIdentityStore::GetCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identitystore.h
api_name:
 - IIdentityStore.GetCount
---

# IIdentityStore::GetCount


## -description

The <b>GetCount</b> method gets the number of identity providers registered on the system.

## -parameters

### -param pdwProviders [out]

The number of identity providers registered on the system.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/identitystore/nn-identitystore-iidentitystore">IIdentityStore</a>