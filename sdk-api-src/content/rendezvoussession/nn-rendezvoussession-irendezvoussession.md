---
UID: NN:rendezvoussession.IRendezvousSession
title: IRendezvousSession (rendezvoussession.h)
description: Exposes methods that send data about the session and that can terminate it.
helpviewer_keywords: ["IRendezvousSession","IRendezvousSession interface [Remote Assistance]","IRendezvousSession interface [Remote Assistance]","described","remoteassist.remoteassist_IRendezvousSession","remoteassist_IRendezvousSession","rendezvoussession/IRendezvousSession"]
old-location: remoteassist\remoteassist_IRendezvousSession.htm
tech.root: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\ifaces\irendezvoussession\iRendezvousSession.htm
ms.date: 12/05/2018
ms.keywords: IRendezvousSession, IRendezvousSession interface [Remote Assistance], IRendezvousSession interface [Remote Assistance],described, remoteassist.remoteassist_IRendezvousSession, remoteassist_IRendezvousSession, rendezvoussession/IRendezvousSession
req.header: rendezvoussession.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RendezvousSession.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RendezvousSession.tlb
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRendezvousSession
 - rendezvoussession/IRendezvousSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RendezvousSession.tlb
api_name:
 - IRendezvousSession
---

# IRendezvousSession interface


## -description

Exposes methods that send data about the session and that can terminate it.

## -inheritance

The <b>IRendezvousSession</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRendezvousSession</b> also has these types of members:

## -remarks

The instant messaging (IM) application implements this interface and passes the object that implements <b>IRendezvousSession</b> and supports the <a href="/previous-versions/ms715092(v=vs.85)">DRendezvousSessionEvents</a> connection point. 

The Windows Remote Assistance application calls <b>IRendezvousSession</b>-&gt;<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> to retain the session after the call to <a href="/previous-versions/windows/desktop/api/rendezvoussession/nf-rendezvoussession-irendezvousapplication-setrendezvoussession">SetRendezvousSession</a> completes. 

The Windows Remote Assistance application calls <b>IRendezvousSession</b>-&gt;<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when the session is complete.
