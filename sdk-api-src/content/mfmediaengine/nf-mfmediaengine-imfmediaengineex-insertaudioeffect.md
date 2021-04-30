---
UID: NF:mfmediaengine.IMFMediaEngineEx.InsertAudioEffect
title: IMFMediaEngineEx::InsertAudioEffect (mfmediaengine.h)
description: Inserts an audio effect.
helpviewer_keywords: ["FALSE","IMFMediaEngineEx interface [Media Foundation]","InsertAudioEffect method","IMFMediaEngineEx.InsertAudioEffect","IMFMediaEngineEx::InsertAudioEffect","InsertAudioEffect","InsertAudioEffect method [Media Foundation]","InsertAudioEffect method [Media Foundation]","IMFMediaEngineEx interface","TRUE","mf.imfmediaengineex_insertaudioeffect","mfmediaengine/IMFMediaEngineEx::InsertAudioEffect"]
old-location: mf\imfmediaengineex_insertaudioeffect.htm
tech.root: mf
ms.assetid: 0D9ED497-A991-473F-A775-CA780A1E0E06
ms.date: 12/05/2018
ms.keywords: FALSE, IMFMediaEngineEx interface [Media Foundation],InsertAudioEffect method, IMFMediaEngineEx.InsertAudioEffect, IMFMediaEngineEx::InsertAudioEffect, InsertAudioEffect, InsertAudioEffect method [Media Foundation], InsertAudioEffect method [Media Foundation],IMFMediaEngineEx interface, TRUE, mf.imfmediaengineex_insertaudioeffect, mfmediaengine/IMFMediaEngineEx::InsertAudioEffect
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngineEx::InsertAudioEffect
 - mfmediaengine/IMFMediaEngineEx::InsertAudioEffect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.InsertAudioEffect
---

# IMFMediaEngineEx::InsertAudioEffect


## -description

Inserts an audio effect.

## -parameters

### -param pEffect [in]

One of the following: 

<ul>
<li>A pointer to the <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface of a Media Foundation transform (MFT) that implements the audio effect.</li>
<li>A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface of an activation object. The activation object must create an MFT for the audio effect.</li>
</ul>

### -param fOptional [in]

Specifies whether the effect is optional.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The effect is optional. If the Media Engine cannot add the effect, it ignores the effect and  continues playback.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The effect is required. If the Media Engine object cannot add the effect, a playback error occurs.

</td>
</tr>
</table>

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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of audio effects was reached.

</td>
</tr>
</table>

## -remarks

The effect is applied when the next media resource is loaded.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>