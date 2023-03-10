---
UID: NF:mfidl.IMFMediaSession.Stop
title: IMFMediaSession::Stop (mfidl.h)
description: Stops the Media Session.
helpviewer_keywords: ["9cc769cc-24ef-4790-a10e-4aec8fb4fc1f","IMFMediaSession interface [Media Foundation]","Stop method","IMFMediaSession.Stop","IMFMediaSession::Stop","Stop","Stop method [Media Foundation]","Stop method [Media Foundation]","IMFMediaSession interface","mf.imfmediasession_stop","mfidl/IMFMediaSession::Stop"]
old-location: mf\imfmediasession_stop.htm
tech.root: mf
ms.assetid: 9cc769cc-24ef-4790-a10e-4aec8fb4fc1f
ms.date: 12/05/2018
ms.keywords: 9cc769cc-24ef-4790-a10e-4aec8fb4fc1f, IMFMediaSession interface [Media Foundation],Stop method, IMFMediaSession.Stop, IMFMediaSession::Stop, Stop, Stop method [Media Foundation], Stop method [Media Foundation],IMFMediaSession interface, mf.imfmediasession_stop, mfidl/IMFMediaSession::Stop
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
 - IMFMediaSession::Stop
 - mfidl/IMFMediaSession::Stop
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
 - IMFMediaSession.Stop
---

# IMFMediaSession::Stop


## -description

Stops the Media Session.



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
</table>

## -remarks

This method is asynchronous. When the operation completes, the Media Session sends an <a href="/windows/desktop/medfound/mesessionstopped">MESessionStopped</a> event.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession">IMFMediaSession</a>
