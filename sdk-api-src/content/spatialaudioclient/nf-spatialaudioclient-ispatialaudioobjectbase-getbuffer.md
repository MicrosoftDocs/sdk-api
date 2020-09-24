---
UID: NF:spatialaudioclient.ISpatialAudioObjectBase.GetBuffer
title: ISpatialAudioObjectBase::GetBuffer (spatialaudioclient.h)
description: Gets a buffer that is used to supply the audio data for the ISpatialAudioObject.
helpviewer_keywords: ["GetBuffer","GetBuffer method [Core Audio]","GetBuffer method [Core Audio]","ISpatialAudioObjectBase interface","ISpatialAudioObjectBase interface [Core Audio]","GetBuffer method","ISpatialAudioObjectBase.GetBuffer","ISpatialAudioObjectBase::GetBuffer","coreaudio.ispatialaudioobject_getbuffer","spatialaudioclient/ISpatialAudioObjectBase::GetBuffer"]
old-location: coreaudio\ispatialaudioobject_getbuffer.htm
tech.root: CoreAudio
ms.assetid: CD777E2D-4CA0-4C2D-A475-22BF770DD59D
ms.date: 12/05/2018
ms.keywords: GetBuffer, GetBuffer method [Core Audio], GetBuffer method [Core Audio],ISpatialAudioObjectBase interface, ISpatialAudioObjectBase interface [Core Audio],GetBuffer method, ISpatialAudioObjectBase.GetBuffer, ISpatialAudioObjectBase::GetBuffer, coreaudio.ispatialaudioobject_getbuffer, spatialaudioclient/ISpatialAudioObjectBase::GetBuffer
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
 - ISpatialAudioObjectBase::GetBuffer
 - spatialaudioclient/ISpatialAudioObjectBase::GetBuffer
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
 - ISpatialAudioObjectBase.GetBuffer
---

# ISpatialAudioObjectBase::GetBuffer


## -description

Gets a buffer that is used to supply the audio data for the <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a>.

## -parameters

### -param buffer [out]

The buffer into which audio data is written.

### -param bufferLength [out]

The length of the buffer in bytes. This length will be the value returned in the   <i>frameCountPerBuffer</i> parameter to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> multiplied by the value of the <b>nBlockAlign</b> field of the <a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a> structure passed in the     <a href="/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams">SpatialAudioObjectRenderStreamActivationParams</a>  
    parameter to  <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a>.

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

<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> was not called before the call to <b>GetBuffer</b>. This method must be called before the first time <b>GetBuffer</b> is called and after every subsequent call to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects">ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects</a>.

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

The first time <b>GetBuffer</b> is called after the <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> is activated with a call <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject</a>,  
    lifetime of the spatial audio object starts.  
    To keep the spatial audio object alive after that, this <b>GetBuffer</b> must be called on every processing pass (between calls to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> and <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects">ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects</a>). If <b>GetBuffer</b> is not called within an audio processing pass, <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream">SetEndOfStream</a> is called implicitly on the audio object to deactivate, and the audio object can only be reused after calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the object and then reactivating the object by calling <b>ActivateSpatialAudioObject</b> again.

The pointers retrieved by <b>GetBuffer</b> should not be used after   
    <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects">ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects</a> has been called.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a>



<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a>