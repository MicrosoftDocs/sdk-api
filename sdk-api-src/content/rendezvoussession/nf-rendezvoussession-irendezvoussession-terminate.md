---
UID: NF:rendezvoussession.IRendezvousSession.Terminate
title: IRendezvousSession::Terminate
author: windows-driver-content
description: Terminates the remote RendezvousApplication.
old-location: remoteassist\remoteassist_IRendezvousSession_Terminate.htm
old-project: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\ifaces\irendezvoussession\terminate.htm
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IRendezvousSession interface [Remote Assistance],Terminate method, IRendezvousSession.Terminate, IRendezvousSession::Terminate, Terminate, Terminate method [Remote Assistance], Terminate method [Remote Assistance],IRendezvousSession interface, remoteassist.remoteassist_IRendezvousSession_Terminate, remoteassist_IRendezvousSession_Terminate, rendezvoussession/IRendezvousSession::Terminate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RendezvousSession.tlb
api_name:
-	IRendezvousSession.Terminate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRendezvousSession::Terminate


## -description


Terminates the remote <a href="https://msdn.microsoft.com/306efb96-5193-410d-b2f8-e71453828a5e">RendezvousApplication</a>.


## -parameters




### -param hr




### -param bstrAppData [in]

Application data. 


#### - HRESULT [in]

The <b>HRESULT</b> from the application termination. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



