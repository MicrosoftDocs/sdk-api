---
UID: NF:rendezvoussession.IRendezvousApplication.SetRendezvousSession
title: IRendezvousApplication::SetRendezvousSession
author: windows-sdk-content
description: Passes IRendezvousSession to the Windows Remote Assistance application. This method is used by the instant messaging application.
old-location: remoteassist\remoteassist_IRendezvousApplication_SetRendezvousSession.htm
old-project: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\ifaces\irendezvousapplication\setRendezvousSession.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IRendezvousApplication interface [Remote Assistance],SetRendezvousSession method, IRendezvousApplication.SetRendezvousSession, IRendezvousApplication::SetRendezvousSession, SetRendezvousSession, SetRendezvousSession method [Remote Assistance], SetRendezvousSession method [Remote Assistance],IRendezvousApplication interface, remoteassist.remoteassist_IRendezvousApplication_SetRendezvousSession, remoteassist_IRendezvousApplication_SetRendezvousSession, remoteassist_IRendezvousApplicationremoteassist_IRendezvousApplication_SetRendezvousSession_cpp, rendezvoussession/IRendezvousApplication::SetRendezvousSession
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
 - IRendezvousApplication.SetRendezvousSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IRendezvousApplication::SetRendezvousSession


## -description


Passes <a href="https://msdn.microsoft.com/3e6dc5c7-2238-4ea8-a4fb-75e4b56d3cfd">IRendezvousSession</a> to the Windows Remote Assistance application. This method is used by the instant messaging application. 


## -parameters




### -param pRendezvousSession [in]

<a href="https://msdn.microsoft.com/3e6dc5c7-2238-4ea8-a4fb-75e4b56d3cfd">IRendezvousSession</a>

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
The <a href="https://msdn.microsoft.com/3e6dc5c7-2238-4ea8-a4fb-75e4b56d3cfd">IRendezvousSession</a> was passed to the Windows Remote Assistance application successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The session object passed to the method is not valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
A catastrophic error occurred while trying to pass the session to the Windows Remote Assistance application.

</td>
</tr>
</table>
 



