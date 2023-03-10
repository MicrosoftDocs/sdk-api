---
UID: NF:mfidl.IMFMediaSink.GetPresentationClock
title: IMFMediaSink::GetPresentationClock (mfidl.h)
description: Gets the presentation clock that was set on the media sink.
helpviewer_keywords: ["GetPresentationClock","GetPresentationClock method [Media Foundation]","GetPresentationClock method [Media Foundation]","IMFMediaSink interface","IMFMediaSink interface [Media Foundation]","GetPresentationClock method","IMFMediaSink.GetPresentationClock","IMFMediaSink::GetPresentationClock","ffa6a7b5-cd79-4c45-a5e3-9d133ffc89a6","mf.imfmediasink_getpresentationclock","mfidl/IMFMediaSink::GetPresentationClock"]
old-location: mf\imfmediasink_getpresentationclock.htm
tech.root: mf
ms.assetid: ffa6a7b5-cd79-4c45-a5e3-9d133ffc89a6
ms.date: 12/05/2018
ms.keywords: GetPresentationClock, GetPresentationClock method [Media Foundation], GetPresentationClock method [Media Foundation],IMFMediaSink interface, IMFMediaSink interface [Media Foundation],GetPresentationClock method, IMFMediaSink.GetPresentationClock, IMFMediaSink::GetPresentationClock, ffa6a7b5-cd79-4c45-a5e3-9d133ffc89a6, mf.imfmediasink_getpresentationclock, mfidl/IMFMediaSink::GetPresentationClock
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFMediaSink::GetPresentationClock
 - mfidl/IMFMediaSink::GetPresentationClock
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
 - IMFMediaSink.GetPresentationClock
---

# IMFMediaSink::GetPresentationClock


## -description

Gets the presentation clock that was set on the media sink.

## -parameters

### -param ppPresentationClock [out]

Receives a pointer to the presentation clock's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a> interface. The caller must release the interface.

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
<dt><b>MF_E_NO_CLOCK</b></dt>
</dl>
</td>
<td width="60%">
No clock has been set. To set the presentation clock, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-setpresentationclock">IMFMediaSink::SetPresentationClock</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown">Shutdown</a> method has been called.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>