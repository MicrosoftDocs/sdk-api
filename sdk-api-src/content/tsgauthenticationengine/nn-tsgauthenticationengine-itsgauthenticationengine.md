---
UID: NN:tsgauthenticationengine.ITSGAuthenticationEngine
title: ITSGAuthenticationEngine (tsgauthenticationengine.h)
description: Exposes methods that authenticate users for Remote Desktop Gateway (RD Gateway).
helpviewer_keywords: ["ITSGAuthenticationEngine","ITSGAuthenticationEngine interface [Remote Desktop Services]","ITSGAuthenticationEngine interface [Remote Desktop Services]","described","termserv.itsgauthenticationengine","tsgauthenticationengine/ITSGAuthenticationEngine"]
old-location: termserv\itsgauthenticationengine.htm
tech.root: TermServ
ms.assetid: c72f3f22-a403-45b0-9ccb-6339ae001024
ms.date: 12/05/2018
ms.keywords: ITSGAuthenticationEngine, ITSGAuthenticationEngine interface [Remote Desktop Services], ITSGAuthenticationEngine interface [Remote Desktop Services],described, termserv.itsgauthenticationengine, tsgauthenticationengine/ITSGAuthenticationEngine
req.header: tsgauthenticationengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGAuthenticationEngine.idl
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
 - ITSGAuthenticationEngine
 - tsgauthenticationengine/ITSGAuthenticationEngine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGAuthenticationEngine.h
api_name:
 - ITSGAuthenticationEngine
---

# ITSGAuthenticationEngine interface


## -description

Exposes methods that authenticate users for Remote Desktop Gateway (RD Gateway). Implement this interface when you want to override the default authentication process in RD Gateway.

## -inheritance

The <b>ITSGAuthenticationEngine</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITSGAuthenticationEngine</b> also has these types of members:

