---
UID: NN:rendezvoussession.IRendezvousApplication
title: IRendezvousApplication
author: windows-sdk-content
description: Exposes a method used by an instant messaging (IM) application to create a remote assistance session.
old-location: remoteassist\remoteassist_IRendezvousApplication.htm
tech.root: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\ifaces\irendezvousapplication\irendezvousapplication.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IRendezvousApplication, IRendezvousApplication interface [Remote Assistance], IRendezvousApplication interface [Remote Assistance],described, remoteassist.remoteassist_IRendezvousApplication, remoteassist_IRendezvousApplication, rendezvoussession/IRendezvousApplication
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRendezvousApplication interface


## -description


Exposes a method used by an instant messaging (IM) application to create a remote assistance session. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRendezvousApplication</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRendezvousApplication</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/08144565-a382-4d61-9e23-011e60b06957">SetRendezvousSession</a>
</td>
<td align="left" width="63%">
Passes <a href="https://msdn.microsoft.com/3e6dc5c7-2238-4ea8-a4fb-75e4b56d3cfd">IRendezvousSession</a> to the Windows Remote Assistance application. This method is used by the instant messaging application. 

</td>
</tr>
</table> 


## -remarks



After an IM contact has accepted the remote assistance invitation, the IM application must instantiate the Windows Remote Assistance application on both sides of the connection by calling <a href="http://msdn.microsoft.com/en-us/library/ms686615(VS.85).aspx">CoCreateInstance</a> on the Windows Remote Assistance application's <b>IRendezvousApplication</b> interface. 

The IM application calls the <a href="https://msdn.microsoft.com/08144565-a382-4d61-9e23-011e60b06957">SetRendezvousSession</a> method to pass its implementation of the <a href="https://msdn.microsoft.com/3e6dc5c7-2238-4ea8-a4fb-75e4b56d3cfd">IRendezvousSession</a> interface to the Windows Remote Assistance application. 



