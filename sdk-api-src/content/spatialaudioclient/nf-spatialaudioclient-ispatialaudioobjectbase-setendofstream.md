---
UID: NF:spatialaudioclient.ISpatialAudioObjectBase.SetEndOfStream
title: ISpatialAudioObjectBase::SetEndOfStream (spatialaudioclient.h)
description: Instructs the system that the final block of audio data has been submitted for the ISpatialAudioObject so that the object can be deactivated and its resources reused.
helpviewer_keywords: ["ISpatialAudioObjectBase interface [Core Audio]","SetEndOfStream method","ISpatialAudioObjectBase.SetEndOfStream","ISpatialAudioObjectBase::SetEndOfStream","SetEndOfStream","SetEndOfStream method [Core Audio]","SetEndOfStream method [Core Audio]","ISpatialAudioObjectBase interface","coreaudio.ispatialaudioobject_setendofstream","spatialaudioclient/ISpatialAudioObjectBase::SetEndOfStream"]
old-location: coreaudio\ispatialaudioobject_setendofstream.htm
tech.root: CoreAudio
ms.assetid: 17294E5D-04D7-43B9-AD41-392344309308
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectBase interface [Core Audio],SetEndOfStream method, ISpatialAudioObjectBase.SetEndOfStream, ISpatialAudioObjectBase::SetEndOfStream, SetEndOfStream, SetEndOfStream method [Core Audio], SetEndOfStream method [Core Audio],ISpatialAudioObjectBase interface, coreaudio.ispatialaudioobject_setendofstream, spatialaudioclient/ISpatialAudioObjectBase::SetEndOfStream
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
 - ISpatialAudioObjectBase::SetEndOfStream
 - spatialaudioclient/ISpatialAudioObjectBase::SetEndOfStream
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
 - ISpatialAudioObjectBase.SetEndOfStream
---

# ISpatialAudioObjectBase::SetEndOfStream


## -description

Instructs the system that the final block of audio data has been  submitted for the <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> so that the object can be deactivated and its resources reused.

## -parameters

### -param frameCount [in]

The number of audio frames in the audio buffer that should be included in the final processing pass. This number may be smaller than or equal to the value returned in  the <i>frameCountPerBuffer</i> parameter to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a>.

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
<dt><b>SPTLAUDCLNT_E_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetEndOfStream</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_RESOURCES_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream">SetEndOfStream</a> was called either explicitly or implicitly in a previous audio processing pass. <b>SetEndOfStream</b> is called implicitly by the system if <b>GetBuffer</b> is not called within an audio processing pass (between calls to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> and <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects">ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects</a>).

</td>
</tr>
</table>

## -remarks

Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> after calling <b>SetEndOfStream</b> to make free the audio object resources for future use.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a>



<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a>