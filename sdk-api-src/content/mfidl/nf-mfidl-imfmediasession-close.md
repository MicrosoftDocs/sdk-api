---
UID: NF:mfidl.IMFMediaSession.Close
title: IMFMediaSession::Close (mfidl.h)
description: Closes the Media Session and releases all of the resources it is using.
helpviewer_keywords: ["6ed118ae-7538-4ef6-81fc-b762f709838f","Close","Close method [Media Foundation]","Close method [Media Foundation]","IMFMediaSession interface","IMFMediaSession interface [Media Foundation]","Close method","IMFMediaSession.Close","IMFMediaSession::Close","mf.imfmediasession_close","mfidl/IMFMediaSession::Close"]
old-location: mf\imfmediasession_close.htm
tech.root: mf
ms.assetid: 6ed118ae-7538-4ef6-81fc-b762f709838f
ms.date: 12/05/2018
ms.keywords: 6ed118ae-7538-4ef6-81fc-b762f709838f, Close, Close method [Media Foundation], Close method [Media Foundation],IMFMediaSession interface, IMFMediaSession interface [Media Foundation],Close method, IMFMediaSession.Close, IMFMediaSession::Close, mf.imfmediasession_close, mfidl/IMFMediaSession::Close
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
 - IMFMediaSession::Close
 - mfidl/IMFMediaSession::Close
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
 - IMFMediaSession.Close
---

# IMFMediaSession::Close


## -description

Closes the Media Session and releases all of the resources it is using.



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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The Media Session has been shut down.

</td>
</tr>
</table>

## -remarks

This method is asynchronous. When the operation completes, the Media Session sends an <a href="/windows/desktop/medfound/mesessionclosed">MESessionClosed</a> event.

After the <b>Close</b> method is called, the only valid methods on the Media Session are the following:

<ul>
<li>

<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock">IMFMediaSession::GetClock</a>


</li>
<li>

<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getfulltopology">IMFMediaSession::GetFullTopology</a>


</li>
<li>

<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities">IMFMediaSession::GetSessionCapabilities</a>


</li>
<li>

<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown">IMFMediaSession::Shutdown</a>


</li>
</ul>
All other methods return MF_E_INVALIDREQUEST, or else queue an event with that error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession">IMFMediaSession</a>
