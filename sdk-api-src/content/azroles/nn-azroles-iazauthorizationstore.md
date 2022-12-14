---
UID: NN:azroles.IAzAuthorizationStore
title: IAzAuthorizationStore (azroles.h)
description: Defines the container that is the root of the authorization policy store.
helpviewer_keywords: ["IAzAuthorizationStore","IAzAuthorizationStore interface [Security]","IAzAuthorizationStore interface [Security]","described","azroles/IAzAuthorizationStore","security.azauthorizationstore"]
old-location: security\azauthorizationstore.htm
tech.root: security
ms.assetid: f848cca6-3838-46bc-b1f4-d6eab5096046
ms.date: 12/05/2018
ms.keywords: IAzAuthorizationStore, IAzAuthorizationStore interface [Security], IAzAuthorizationStore interface [Security],described, azroles/IAzAuthorizationStore, security.azauthorizationstore
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
 - IAzAuthorizationStore
 - azroles/IAzAuthorizationStore
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
 - IAzAuthorizationStore
---

# IAzAuthorizationStore interface


## -description

The <b>AzAuthorizationStore</b> object defines the container that is the root of the authorization policy store.

## -inheritance

The <b>IAzAuthorizationStore</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAzAuthorizationStore</b> also has these types of members:

## -remarks

The <b>AzAuthorizationStore</b> object is named according to the URL passed to the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-initialize">Initialize</a> method. The object has no name within  the policy store.

The application must ensure that the user context from which the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-initialize">Initialize</a> method is called is used for all future access to the <b>AzAuthorizationStore</b> object, except for the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken">IAzApplication::InitializeClientContextFromToken</a> method.

<div class="alert"><b>Note</b>  If an XML store is used over a network, the traffic is not automatically encrypted. IPsec can be used to encrypt the authorization information in transit.</div>
<div> </div>
