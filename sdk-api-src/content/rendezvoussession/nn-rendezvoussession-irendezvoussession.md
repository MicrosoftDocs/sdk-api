---
UID: NN:rendezvoussession.IRendezvousSession
title: IRendezvousSession (rendezvoussession.h)
author: windows-sdk-content
description: Exposes methods that send data about the session and that can terminate it.
old-location: remoteassist\remoteassist_IRendezvousSession.htm
tech.root: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\ifaces\irendezvoussession\iRendezvousSession.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRendezvousSession, IRendezvousSession interface [Remote Assistance], IRendezvousSession interface [Remote Assistance],described, remoteassist.remoteassist_IRendezvousSession, remoteassist_IRendezvousSession, rendezvoussession/IRendezvousSession
ms.topic: interface
f1_keywords: ["rendezvoussession/IRendezvousSession"]
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
ms.custom: 19H1
---

# IRendezvousSession interface


## -description


Exposes methods that send data about the session and that can terminate it.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRendezvousSession</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRendezvousSession</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/rendezvoussession/nf-rendezvoussession-irendezvoussession-sendcontextdata">SendContextData</a>
</td>
<td align="left" width="63%">
Sends the context data to the remote <a href="https://docs.microsoft.com/previous-versions/windows/desktop/remoteassist/remoteassist-rendezvousapplication">RendezvousApplication</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/rendezvoussession/nf-rendezvoussession-irendezvoussession-terminate">Terminate</a>
</td>
<td align="left" width="63%">
Terminates the remote <a href="https://docs.microsoft.com/previous-versions/windows/desktop/remoteassist/remoteassist-rendezvousapplication">RendezvousApplication</a>.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/rendezvoussession/nf-rendezvoussession-irendezvoussession-get_flags">Flags</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/rendezvoussession/nf-rendezvoussession-irendezvoussession-get_remoteuser">RemoteUser</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/rendezvoussession/nf-rendezvoussession-irendezvoussession-get_state">State</a>


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



The instant messaging (IM) application implements this interface and passes the object that implements <b>IRendezvousSession</b> and supports the <a href="https://docs.microsoft.com/previous-versions/ms715092(v=vs.85)">DRendezvousSessionEvents</a> connection point. 

The Windows Remote Assistance application calls <b>IRendezvousSession</b>-&gt;<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> to retain the session after the call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/rendezvoussession/nf-rendezvoussession-irendezvousapplication-setrendezvoussession">SetRendezvousSession</a> completes. 

The Windows Remote Assistance application calls <b>IRendezvousSession</b>-&gt;<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when the session is complete. 



