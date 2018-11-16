---
UID: NN:rendezvoussession.IRendezvousSession
title: IRendezvousSession
author: windows-sdk-content
description: Exposes methods that send data about the session and that can terminate it.
old-location: remoteassist\remoteassist_IRendezvousSession.htm
tech.root: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\ifaces\irendezvoussession\iRendezvousSession.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IRendezvousSession, IRendezvousSession interface [Remote Assistance], IRendezvousSession interface [Remote Assistance],described, remoteassist.remoteassist_IRendezvousSession, remoteassist_IRendezvousSession, rendezvoussession/IRendezvousSession
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IRendezvousSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRendezvousSession interface


## -description


Exposes methods that send data about the session and that can terminate it.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRendezvousSession</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRendezvousSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRendezvousSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5908accc-c8c2-4ca5-b76e-5c62e8a36c67">SendContextData</a>
</td>
<td align="left" width="63%">
Sends the context data to the remote <a href="https://msdn.microsoft.com/306efb96-5193-410d-b2f8-e71453828a5e">RendezvousApplication</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a77c6f25-fbb7-46af-8b15-a4ed55f69273">Terminate</a>
</td>
<td align="left" width="63%">
Terminates the remote <a href="https://msdn.microsoft.com/306efb96-5193-410d-b2f8-e71453828a5e">RendezvousApplication</a>.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRendezvousSession</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7252098d-71f2-43b8-a0ae-a42a22de247f">Flags</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates session information. For example, the session flag can indicate whether the user is the inviter or the invitee. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/23288533-69ab-4217-ba54-07af3811fa91">RemoteUser</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a pointer to a <b>BSTR</b> that contains the Windows Messenger contact name. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/587fa190-937b-465b-bc5b-1cdc23902053">State</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates the session state. 

</td>
</tr>
</table> 


## -remarks



The instant messaging (IM) application implements this interface and passes the object that implements <b>IRendezvousSession</b> and supports the <a href="https://msdn.microsoft.com/f0261091-416d-45db-b102-2346c2252d6a">DRendezvousSessionEvents</a> connection point. 

The Windows Remote Assistance application calls <b>IRendezvousSession</b>-&gt;<a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> to retain the session after the call to <a href="https://msdn.microsoft.com/08144565-a382-4d61-9e23-011e60b06957">SetRendezvousSession</a> completes. 

The Windows Remote Assistance application calls <b>IRendezvousSession</b>-&gt;<a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> when the session is complete. 



