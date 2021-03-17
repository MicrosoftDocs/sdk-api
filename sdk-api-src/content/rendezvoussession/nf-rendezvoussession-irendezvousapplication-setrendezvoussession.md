---
UID: NF:rendezvoussession.IRendezvousApplication.SetRendezvousSession
title: IRendezvousApplication::SetRendezvousSession (rendezvoussession.h)
description: Passes IRendezvousSession to the Windows Remote Assistance application. This method is used by the instant messaging application.
helpviewer_keywords: ["IRendezvousApplication interface [Remote Assistance]","SetRendezvousSession method","IRendezvousApplication.SetRendezvousSession","IRendezvousApplication::SetRendezvousSession","SetRendezvousSession","SetRendezvousSession method [Remote Assistance]","SetRendezvousSession method [Remote Assistance]","IRendezvousApplication interface","remoteassist.remoteassist_IRendezvousApplication_SetRendezvousSession","remoteassist_IRendezvousApplication_SetRendezvousSession","remoteassist_IRendezvousApplicationremoteassist_IRendezvousApplication_SetRendezvousSession_cpp","rendezvoussession/IRendezvousApplication::SetRendezvousSession"]
old-location: remoteassist\remoteassist_IRendezvousApplication_SetRendezvousSession.htm
tech.root: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\ifaces\irendezvousapplication\setRendezvousSession.htm
ms.date: 12/05/2018
ms.keywords: IRendezvousApplication interface [Remote Assistance],SetRendezvousSession method, IRendezvousApplication.SetRendezvousSession, IRendezvousApplication::SetRendezvousSession, SetRendezvousSession, SetRendezvousSession method [Remote Assistance], SetRendezvousSession method [Remote Assistance],IRendezvousApplication interface, remoteassist.remoteassist_IRendezvousApplication_SetRendezvousSession, remoteassist_IRendezvousApplication_SetRendezvousSession, remoteassist_IRendezvousApplicationremoteassist_IRendezvousApplication_SetRendezvousSession_cpp, rendezvoussession/IRendezvousApplication::SetRendezvousSession
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
 - IRendezvousApplication::SetRendezvousSession
 - rendezvoussession/IRendezvousApplication::SetRendezvousSession
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
 - IRendezvousApplication.SetRendezvousSession
---

# IRendezvousApplication::SetRendezvousSession


## -description

Passes <a href="/previous-versions/windows/desktop/api/rendezvoussession/nn-rendezvoussession-irendezvoussession">IRendezvousSession</a> to the Windows Remote Assistance application. This method is used by the instant messaging application.

## -parameters

### -param pRendezvousSession [in]

<a href="/previous-versions/windows/desktop/api/rendezvoussession/nn-rendezvoussession-irendezvoussession">IRendezvousSession</a>

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
The <a href="/previous-versions/windows/desktop/api/rendezvoussession/nn-rendezvoussession-irendezvoussession">IRendezvousSession</a> was passed to the Windows Remote Assistance application successfully. 

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