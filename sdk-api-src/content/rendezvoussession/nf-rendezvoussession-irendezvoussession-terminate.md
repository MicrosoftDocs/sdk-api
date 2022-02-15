---
UID: NF:rendezvoussession.IRendezvousSession.Terminate
title: IRendezvousSession::Terminate (rendezvoussession.h)
description: Terminates the remote RendezvousApplication.
helpviewer_keywords: ["IRendezvousSession interface [Remote Assistance]","Terminate method","IRendezvousSession.Terminate","IRendezvousSession::Terminate","Terminate","Terminate method [Remote Assistance]","Terminate method [Remote Assistance]","IRendezvousSession interface","remoteassist.remoteassist_IRendezvousSession_Terminate","remoteassist_IRendezvousSession_Terminate","rendezvoussession/IRendezvousSession::Terminate"]
old-location: remoteassist\remoteassist_IRendezvousSession_Terminate.htm
tech.root: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\ifaces\irendezvoussession\terminate.htm
ms.date: 12/05/2018
ms.keywords: IRendezvousSession interface [Remote Assistance],Terminate method, IRendezvousSession.Terminate, IRendezvousSession::Terminate, Terminate, Terminate method [Remote Assistance], Terminate method [Remote Assistance],IRendezvousSession interface, remoteassist.remoteassist_IRendezvousSession_Terminate, remoteassist_IRendezvousSession_Terminate, rendezvoussession/IRendezvousSession::Terminate
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
 - IRendezvousSession::Terminate
 - rendezvoussession/IRendezvousSession::Terminate
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
 - IRendezvousSession.Terminate
---

# IRendezvousSession::Terminate


## -description

Terminates the remote <a href="/previous-versions/windows/desktop/remoteassist/remoteassist-rendezvousapplication">RendezvousApplication</a>.

## -parameters

### -param hr [in]

The <b>HRESULT</b> from the application termination.

### -param bstrAppData [in]

Application data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.