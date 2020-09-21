---
UID: NF:mfidl.IMFTimecodeTranslate.BeginConvertHNSToTimecode
title: IMFTimecodeTranslate::BeginConvertHNSToTimecode (mfidl.h)
description: Starts an asynchronous call to convert time in 100-nanosecond units to Society of Motion Picture and Television Engineers (SMPTE) time code.
helpviewer_keywords: ["BeginConvertHNSToTimecode","BeginConvertHNSToTimecode method [Media Foundation]","BeginConvertHNSToTimecode method [Media Foundation]","IMFTimecodeTranslate interface","IMFTimecodeTranslate interface [Media Foundation]","BeginConvertHNSToTimecode method","IMFTimecodeTranslate.BeginConvertHNSToTimecode","IMFTimecodeTranslate::BeginConvertHNSToTimecode","mf.imftimecodetranslate_beginconverthnstotimecode","mfidl/IMFTimecodeTranslate::BeginConvertHNSToTimecode"]
old-location: mf\imftimecodetranslate_beginconverthnstotimecode.htm
tech.root: mf
ms.assetid: 42b5de27-aaa6-4bd9-b2b0-3aeabfc28ef2
ms.date: 12/05/2018
ms.keywords: BeginConvertHNSToTimecode, BeginConvertHNSToTimecode method [Media Foundation], BeginConvertHNSToTimecode method [Media Foundation],IMFTimecodeTranslate interface, IMFTimecodeTranslate interface [Media Foundation],BeginConvertHNSToTimecode method, IMFTimecodeTranslate.BeginConvertHNSToTimecode, IMFTimecodeTranslate::BeginConvertHNSToTimecode, mf.imftimecodetranslate_beginconverthnstotimecode, mfidl/IMFTimecodeTranslate::BeginConvertHNSToTimecode
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFTimecodeTranslate::BeginConvertHNSToTimecode
 - mfidl/IMFTimecodeTranslate::BeginConvertHNSToTimecode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFTimecodeTranslate.BeginConvertHNSToTimecode
---

# IMFTimecodeTranslate::BeginConvertHNSToTimecode


## -description

Starts an asynchronous call to convert time in 100-nanosecond units to Society of Motion Picture and Television Engineers (SMPTE) time code.

## -parameters

### -param hnsTime [in]

The time to convert, in 100-nanosecond units.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param punkState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The object's <b>Shutdown</b> method was called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BYTESTREAM_NOT_SEEKABLE</b></dt>
</dl>
</td>
<td width="60%">
The byte stream is not seekable. The time code cannot be read from the end of the byte stream.

</td>
</tr>
</table>

## -remarks

When the asynchronous method completes, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the application must call <a href="/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverthnstotimecode">IMFTimecodeTranslate::EndConvertHNSToTimecode</a> to complete the asynchronous request.

## -see-also

<a href="/windows/desktop/medfound/calling-asynchronous-methods">Calling Asynchronous Methods</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate">IMFTimecodeTranslate</a>



<a href="/windows/desktop/medfound/mftime">MFTIME</a>