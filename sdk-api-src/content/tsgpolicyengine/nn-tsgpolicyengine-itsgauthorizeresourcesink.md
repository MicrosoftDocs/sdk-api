---
UID: NN:tsgpolicyengine.ITSGAuthorizeResourceSink
title: ITSGAuthorizeResourceSink (tsgpolicyengine.h)
description: Exposes methods that notify Remote Desktop Gateway (RD Gateway) about the result of an attempt to authorize a resource.
helpviewer_keywords: ["ITSGAuthorizeResourceSink","ITSGAuthorizeResourceSink interface [Remote Desktop Services]","ITSGAuthorizeResourceSink interface [Remote Desktop Services]","described","termserv.itsgauthorizeresourcesink","tsgpolicyengine/ITSGAuthorizeResourceSink"]
old-location: termserv\itsgauthorizeresourcesink.htm
tech.root: TermServ
ms.assetid: 4656064a-41d9-428c-8260-24eea0ee83cc
ms.date: 12/05/2018
ms.keywords: ITSGAuthorizeResourceSink, ITSGAuthorizeResourceSink interface [Remote Desktop Services], ITSGAuthorizeResourceSink interface [Remote Desktop Services],described, termserv.itsgauthorizeresourcesink, tsgpolicyengine/ITSGAuthorizeResourceSink
req.header: tsgpolicyengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
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
 - ITSGAuthorizeResourceSink
 - tsgpolicyengine/ITSGAuthorizeResourceSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGPolicyEngine.h
api_name:
 - ITSGAuthorizeResourceSink
---

# ITSGAuthorizeResourceSink interface


## -description

Exposes methods that notify Remote Desktop Gateway (RD Gateway) about the result of an  attempt to authorize a resource. The authorization plug-in should not implement this interface because it is already implemented. A pointer to this interface is passed to the authorization plug-in when RD Gateway calls the <a href="/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgpolicyengine-authorizeresource">AuthorizeResource</a> method.

## -inheritance

The <b>ITSGAuthorizeResourceSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITSGAuthorizeResourceSink</b> also has these types of members:

