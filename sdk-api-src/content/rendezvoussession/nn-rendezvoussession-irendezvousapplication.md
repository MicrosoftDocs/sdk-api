---
UID: NN:rendezvoussession.IRendezvousApplication
title: IRendezvousApplication (rendezvoussession.h)
description: Exposes a method used by an instant messaging (IM) application to create a remote assistance session.
helpviewer_keywords: ["IRendezvousApplication","IRendezvousApplication interface [Remote Assistance]","IRendezvousApplication interface [Remote Assistance]","described","remoteassist.remoteassist_IRendezvousApplication","remoteassist_IRendezvousApplication","rendezvoussession/IRendezvousApplication"]
old-location: remoteassist\remoteassist_IRendezvousApplication.htm
tech.root: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\ifaces\irendezvousapplication\irendezvousapplication.htm
ms.date: 12/05/2018
ms.keywords: IRendezvousApplication, IRendezvousApplication interface [Remote Assistance], IRendezvousApplication interface [Remote Assistance],described, remoteassist.remoteassist_IRendezvousApplication, remoteassist_IRendezvousApplication, rendezvoussession/IRendezvousApplication
f1_keywords:
- rendezvoussession/IRendezvousApplication
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- RendezvousSession.tlb
api_name:
- IRendezvousApplication
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRendezvousApplication interface


## -description


Exposes a method used by an instant messaging (IM) application to create a remote assistance session. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRendezvousApplication</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRendezvousApplication</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRendezvousApplication</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/rendezvoussession/nf-rendezvoussession-irendezvousapplication-setrendezvoussession">SetRendezvousSession</a>
</td>
<td align="left" width="63%">
Passes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/rendezvoussession/nn-rendezvoussession-irendezvoussession">IRendezvousSession</a> to the Windows Remote Assistance application. This method is used by the instant messaging application. 

</td>
</tr>
</table> 


## -remarks



After an IM contact has accepted the remote assistance invitation, the IM application must instantiate the Windows Remote Assistance application on both sides of the connection by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> on the Windows Remote Assistance application's <b>IRendezvousApplication</b> interface. 

The IM application calls the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/rendezvoussession/nf-rendezvoussession-irendezvousapplication-setrendezvoussession">SetRendezvousSession</a> method to pass its implementation of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/rendezvoussession/nn-rendezvoussession-irendezvoussession">IRendezvousSession</a> interface to the Windows Remote Assistance application. 



