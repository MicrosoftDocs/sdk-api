---
UID: NF:azroles.IAzAuthorizationStore.Submit
title: IAzAuthorizationStore::Submit (azroles.h)
description: Persists changes made to the AzAuthorizationStore object.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","Submit method","IAzAuthorizationStore interface [Security]","Submit method","IAzAuthorizationStore.Submit","IAzAuthorizationStore::Submit","Submit","Submit method [Security]","Submit method [Security]","AzAuthorizationStore object","Submit method [Security]","IAzAuthorizationStore interface","azroles/IAzAuthorizationStore::Submit","security.azauthorizationstore_submit"]
old-location: security\azauthorizationstore_submit.htm
tech.root: security
ms.assetid: bf2962af-0e8f-4c4c-a63a-dfd623308e4d
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],Submit method, IAzAuthorizationStore interface [Security],Submit method, IAzAuthorizationStore.Submit, IAzAuthorizationStore::Submit, Submit, Submit method [Security], Submit method [Security],AzAuthorizationStore object, Submit method [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::Submit, security.azauthorizationstore_submit
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
 - IAzAuthorizationStore::Submit
 - azroles/IAzAuthorizationStore::Submit
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
 - AzAuthorizationStore.Submit
 - IAzAuthorizationStore.Submit
---

# IAzAuthorizationStore::Submit


## -description

The <b>Submit</b> method persists changes made to the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object.

## -parameters

### -param lFlags [in]

Flags that modify the behavior of the <b>Submit</b> method. The default value is zero. If the AZ_SUBMIT_FLAG_ABORT flag is specified, the changes to the object are discarded and the object is updated to match the underlying policy store.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

Any additions or modifications to an <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object are not persisted until the <b>Submit</b> method is called. The <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-delete">Delete</a>  method automatically submits changes.

The <b>Submit</b> method does not extend to child objects; child objects  must be individually persisted to the policy store. A created <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object must be submitted before it can be referenced or become a parent object. The destructor for an object silently discards unsubmitted changes.