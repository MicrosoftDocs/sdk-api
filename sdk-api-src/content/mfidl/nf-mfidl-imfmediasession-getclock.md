---
UID: NF:mfidl.IMFMediaSession.GetClock
title: IMFMediaSession::GetClock (mfidl.h)
description: Retrieves the Media Session's presentation clock.
helpviewer_keywords: ["16444da2-68f2-4d94-8c6f-9e512d51e5e9","GetClock","GetClock method [Media Foundation]","GetClock method [Media Foundation]","IMFMediaSession interface","IMFMediaSession interface [Media Foundation]","GetClock method","IMFMediaSession.GetClock","IMFMediaSession::GetClock","mf.imfmediasession_getclock","mfidl/IMFMediaSession::GetClock"]
old-location: mf\imfmediasession_getclock.htm
tech.root: mf
ms.assetid: 16444da2-68f2-4d94-8c6f-9e512d51e5e9
ms.date: 12/05/2018
ms.keywords: 16444da2-68f2-4d94-8c6f-9e512d51e5e9, GetClock, GetClock method [Media Foundation], GetClock method [Media Foundation],IMFMediaSession interface, IMFMediaSession interface [Media Foundation],GetClock method, IMFMediaSession.GetClock, IMFMediaSession::GetClock, mf.imfmediasession_getclock, mfidl/IMFMediaSession::GetClock
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
 - IMFMediaSession::GetClock
 - mfidl/IMFMediaSession::GetClock
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
 - IMFMediaSession.GetClock
---

# IMFMediaSession::GetClock


## -description

Retrieves the Media Session's presentation clock.

## -parameters

### -param ppClock [out]

Receives a pointer to the presentation clock's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a> interface. The caller must release the interface.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The Media Session does not have a presentation clock.

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

The application can query the returned <a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a> pointer for the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a> interface. However, the application should not use this interface to control the state of the presentation clock. Instead, the application should always call the transport control methods on the Media Session's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession">IMFMediaSession</a> interface, such as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start">Start</a>, <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop">Stop</a>, and <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause">Pause</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession">IMFMediaSession</a>