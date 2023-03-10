---
UID: NF:mfidl.IMFMediaSession.Pause
title: IMFMediaSession::Pause (mfidl.h)
description: Pauses the Media Session.
helpviewer_keywords: ["IMFMediaSession interface [Media Foundation]","Pause method","IMFMediaSession.Pause","IMFMediaSession::Pause","Pause","Pause method [Media Foundation]","Pause method [Media Foundation]","IMFMediaSession interface","fcc576ba-f8be-4106-a270-756b2abf52d4","mf.imfmediasession_pause","mfidl/IMFMediaSession::Pause"]
old-location: mf\imfmediasession_pause.htm
tech.root: mf
ms.assetid: fcc576ba-f8be-4106-a270-756b2abf52d4
ms.date: 12/05/2018
ms.keywords: IMFMediaSession interface [Media Foundation],Pause method, IMFMediaSession.Pause, IMFMediaSession::Pause, Pause, Pause method [Media Foundation], Pause method [Media Foundation],IMFMediaSession interface, fcc576ba-f8be-4106-a270-756b2abf52d4, mf.imfmediasession_pause, mfidl/IMFMediaSession::Pause
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaSession::Pause
 - mfidl/IMFMediaSession::Pause
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSession.Pause
---

# IMFMediaSession::Pause


## -description

Pauses the Media Session.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The operation cannot be performed in the Media Session's current state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The Media Session has been shut down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SESSION_PAUSEWHILESTOPPED</b></dt>
</dl>
</td>
<td width="60%">
The Media Session cannot pause while stopped.

</td>
</tr>
</table>

## -remarks

This method pauses the presentation clock.

This method is asynchronous. When the operation completes, the Media Session sends an <a href="/windows/desktop/medfound/mesessionpaused">MESessionPaused</a> event.

This method fails if the Media Session is stopped.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession">IMFMediaSession</a>



<a href="/windows/desktop/medfound/mesessionpaused">MESessionPaused</a>
