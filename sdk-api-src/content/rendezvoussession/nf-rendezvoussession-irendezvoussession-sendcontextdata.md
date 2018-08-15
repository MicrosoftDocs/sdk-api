---
UID: NF:rendezvoussession.IRendezvousSession.SendContextData
title: IRendezvousSession::SendContextData
author: windows-sdk-content
description: Sends the context data to the remote RendezvousApplication.
old-location: remoteassist\remoteassist_IRendezvousSession_SendContextData.htm
old-project: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\ifaces\irendezvoussession\sendcontextdata.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IRendezvousSession interface [Remote Assistance],SendContextData method, IRendezvousSession.SendContextData, IRendezvousSession::SendContextData, SendContextData, SendContextData method [Remote Assistance], SendContextData method [Remote Assistance],IRendezvousSession interface, remoteassist.remoteassist_IRendezvousSession_SendContextData, remoteassist_IRendezvousSession_SendContextData, rendezvoussession/IRendezvousSession::SendContextData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rendezvoussession.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RendezvousSession.tlb
api_name:
 - IRendezvousSession.SendContextData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IRendezvousSession::SendContextData


## -description


Sends the context data to the remote <a href="https://msdn.microsoft.com/306efb96-5193-410d-b2f8-e71453828a5e">RendezvousApplication</a>.


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
 



