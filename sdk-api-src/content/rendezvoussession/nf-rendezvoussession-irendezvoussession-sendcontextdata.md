---
UID: NF:rendezvoussession.IRendezvousSession.SendContextData
title: IRendezvousSession::SendContextData (rendezvoussession.h)
description: Sends the context data to the remote RendezvousApplication.
helpviewer_keywords: ["IRendezvousSession interface [Remote Assistance]","SendContextData method","IRendezvousSession.SendContextData","IRendezvousSession::SendContextData","SendContextData","SendContextData method [Remote Assistance]","SendContextData method [Remote Assistance]","IRendezvousSession interface","remoteassist.remoteassist_IRendezvousSession_SendContextData","remoteassist_IRendezvousSession_SendContextData","rendezvoussession/IRendezvousSession::SendContextData"]
old-location: remoteassist\remoteassist_IRendezvousSession_SendContextData.htm
tech.root: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\ifaces\irendezvoussession\sendcontextdata.htm
ms.date: 12/05/2018
ms.keywords: IRendezvousSession interface [Remote Assistance],SendContextData method, IRendezvousSession.SendContextData, IRendezvousSession::SendContextData, SendContextData, SendContextData method [Remote Assistance], SendContextData method [Remote Assistance],IRendezvousSession interface, remoteassist.remoteassist_IRendezvousSession_SendContextData, remoteassist_IRendezvousSession_SendContextData, rendezvoussession/IRendezvousSession::SendContextData
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
 - IRendezvousSession::SendContextData
 - rendezvoussession/IRendezvousSession::SendContextData
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
 - IRendezvousSession.SendContextData
---

# IRendezvousSession::SendContextData


## -description

Sends the context data to the remote <a href="/previous-versions/windows/desktop/remoteassist/remoteassist-rendezvousapplication">RendezvousApplication</a>.

## -parameters

### -param bstrData [in]

A <b>BSTR</b> specifying context data for the application.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The context data was sent successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The context data passed to the method is not valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to send the context data. 

</td>
</tr>
</table>