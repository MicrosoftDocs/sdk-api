---
UID: NF:mfcaptureengine.IMFCaptureSource.SetMirrorState
title: IMFCaptureSource::SetMirrorState (mfcaptureengine.h)
description: Enables or disables mirroring of the video preview stream. (IMFCaptureSource.SetMirrorState)
helpviewer_keywords: ["IMFCaptureSource interface [Media Foundation]","SetMirrorState method","IMFCaptureSource.SetMirrorState","IMFCaptureSource::SetMirrorState","SetMirrorState","SetMirrorState method [Media Foundation]","SetMirrorState method [Media Foundation]","IMFCaptureSource interface","mf.imfcapturesource_setmirrorstate","mf.imfcapturesource_setpreviewmirrorstate","mfcaptureengine/IMFCaptureSource::SetMirrorState"]
old-location: mf\imfcapturesource_setmirrorstate.htm
tech.root: mf
ms.assetid: E170B262-95CD-4434-925A-3573D35FC1DC
ms.date: 12/05/2018
ms.keywords: IMFCaptureSource interface [Media Foundation],SetMirrorState method, IMFCaptureSource.SetMirrorState, IMFCaptureSource::SetMirrorState, SetMirrorState, SetMirrorState method [Media Foundation], SetMirrorState method [Media Foundation],IMFCaptureSource interface, mf.imfcapturesource_setmirrorstate, mf.imfcapturesource_setpreviewmirrorstate, mfcaptureengine/IMFCaptureSource::SetMirrorState
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFCaptureSource::SetMirrorState
 - mfcaptureengine/IMFCaptureSource::SetMirrorState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureSource.SetMirrorState
---

# IMFCaptureSource::SetMirrorState


## -description

Enables or disables mirroring of the video preview stream.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of the stream.

### -param fMirrorState [in]

If   <b>TRUE</b>,    mirroring is enabled; if  <b>FALSE</b>, mirroring is  disabled.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The device stream does not have mirroring capability.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The source is not initialized.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource">IMFCaptureSource</a>
