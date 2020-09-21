---
UID: NF:azroles.IAzAuthorizationStore.Delete
title: IAzAuthorizationStore::Delete (azroles.h)
description: Deletes the policy store currently in use by the AzAuthorizationStore object.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","Delete method","Delete","Delete method [Security]","Delete method [Security]","AzAuthorizationStore object","Delete method [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","Delete method","IAzAuthorizationStore.Delete","IAzAuthorizationStore::Delete","azroles/IAzAuthorizationStore::Delete","security.azauthorizationstore_delete"]
old-location: security\azauthorizationstore_delete.htm
tech.root: security
ms.assetid: 8493af39-c5db-4aeb-839f-bc07e2616443
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],Delete method, Delete, Delete method [Security], Delete method [Security],AzAuthorizationStore object, Delete method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],Delete method, IAzAuthorizationStore.Delete, IAzAuthorizationStore::Delete, azroles/IAzAuthorizationStore::Delete, security.azauthorizationstore_delete
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzAuthorizationStore::Delete
 - azroles/IAzAuthorizationStore::Delete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - AzAuthorizationStore.Delete
 - IAzAuthorizationStore.Delete
---

# IAzAuthorizationStore::Delete


## -description

The <b>Delete</b> method deletes the policy store currently in use by the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object.

## -parameters

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

When the <b>Delete</b> method is called, the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object returns to an uninitialized state. The <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-initialize">Initialize</a> method can then be called to reinitialize the object. 

<div class="alert"><b>Important</b>  All objects opened by clients on the policy store  (for example,  <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> objects created using <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-createapplication">CreateApplication</a>) must be released before you call the <b>Delete</b> method. If the <b>Delete</b> method is called on an <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object whose current policy store contains child objects, HRESULT_FROM_WIN32(ERROR_SERVER_HAS_OPEN_HANDLES) is returned.</div>
<div> </div>