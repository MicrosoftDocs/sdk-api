---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.GetService
title: ISpatialAudioObjectRenderStreamBase::GetService (spatialaudioclient.h)
description: Gets additional services from the ISpatialAudioObjectRenderStream.
helpviewer_keywords: ["GetService","GetService method [Core Audio]","GetService method [Core Audio]","ISpatialAudioObjectRenderStreamBase interface","ISpatialAudioObjectRenderStreamBase interface [Core Audio]","GetService method","ISpatialAudioObjectRenderStreamBase.GetService","ISpatialAudioObjectRenderStreamBase::GetService","coreaudio.ispatialaudioobjectrenderstream_getservice","spatialaudioclient/ISpatialAudioObjectRenderStreamBase::GetService"]
old-location: coreaudio\ispatialaudioobjectrenderstream_getservice.htm
tech.root: CoreAudio
ms.assetid: 9262C9E1-DE15-460C-9BC2-DAD5163F447E
ms.date: 12/05/2018
ms.keywords: GetService, GetService method [Core Audio], GetService method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, ISpatialAudioObjectRenderStreamBase interface [Core Audio],GetService method, ISpatialAudioObjectRenderStreamBase.GetService, ISpatialAudioObjectRenderStreamBase::GetService, coreaudio.ispatialaudioobjectrenderstream_getservice, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::GetService
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ISpatialAudioObjectRenderStreamBase::GetService
 - spatialaudioclient/ISpatialAudioObjectRenderStreamBase::GetService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStreamBase.GetService
---

# ISpatialAudioObjectRenderStreamBase::GetService


## -description

Gets additional services from the <b>ISpatialAudioObjectRenderStream</b>.

## -parameters

### -param riid [in]

The interface ID for the requested service. The client should set this parameter to one of the following REFIID values:

IID_IAudioClock

IID_IAudioClock2

IID_IAudioStreamVolume

### -param service [out]

Pointer to a pointer variable into which the method writes the address of an instance of the requested interface. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method. If the <b>GetService</b> call fails, <i>*ppv </i> is NULL.

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>ppv</i> is NULL.

</td>
</tr>


<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_DESTROYED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient">ISpatialAudioClient</a> associated with the spatial audio stream has been destroyed.

</td>
</tr>


<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>




<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_INTERNAL</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>



<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_UNSUPPORTED_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The media associated with the spatial audio stream uses an unsupported format.

</td>
</tr>
</table>

## -remarks

The <b>GetService</b> method supports the following service interfaces:

<ul>
<li>
<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclock">IAudioClock</a>
</li>
<li>
<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2">IAudioClock2</a>
</li>
<li>
<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiostreamvolume">IAudioStreamVolume</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>



<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a>