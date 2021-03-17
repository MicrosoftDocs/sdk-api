---
UID: NF:mfidl.IMFTimecodeTranslate.BeginConvertTimecodeToHNS
title: IMFTimecodeTranslate::BeginConvertTimecodeToHNS (mfidl.h)
description: Starts an asynchronous call to convert Society of Motion Picture and Television Engineers (SMPTE) time code to 100-nanosecond units.
helpviewer_keywords: ["BeginConvertTimecodeToHNS","BeginConvertTimecodeToHNS method [Media Foundation]","BeginConvertTimecodeToHNS method [Media Foundation]","IMFTimecodeTranslate interface","IMFTimecodeTranslate interface [Media Foundation]","BeginConvertTimecodeToHNS method","IMFTimecodeTranslate.BeginConvertTimecodeToHNS","IMFTimecodeTranslate::BeginConvertTimecodeToHNS","mf.imftimecodetranslate_beginconverttimecodetohns","mfidl/IMFTimecodeTranslate::BeginConvertTimecodeToHNS"]
old-location: mf\imftimecodetranslate_beginconverttimecodetohns.htm
tech.root: mf
ms.assetid: 4e25d5e4-b4d7-4ca4-81c9-12c6d712322d
ms.date: 12/05/2018
ms.keywords: BeginConvertTimecodeToHNS, BeginConvertTimecodeToHNS method [Media Foundation], BeginConvertTimecodeToHNS method [Media Foundation],IMFTimecodeTranslate interface, IMFTimecodeTranslate interface [Media Foundation],BeginConvertTimecodeToHNS method, IMFTimecodeTranslate.BeginConvertTimecodeToHNS, IMFTimecodeTranslate::BeginConvertTimecodeToHNS, mf.imftimecodetranslate_beginconverttimecodetohns, mfidl/IMFTimecodeTranslate::BeginConvertTimecodeToHNS
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
 - IMFTimecodeTranslate::BeginConvertTimecodeToHNS
 - mfidl/IMFTimecodeTranslate::BeginConvertTimecodeToHNS
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
 - IMFTimecodeTranslate.BeginConvertTimecodeToHNS
---

# IMFTimecodeTranslate::BeginConvertTimecodeToHNS


## -description

Starts an asynchronous call to convert Society of Motion Picture and Television Engineers (SMPTE) time code to 100-nanosecond units.

## -parameters

### -param pPropVarTimecode [in]

Time in SMPTE time code to convert. The <b>vt</b> member of the <b>PROPVARIANT</b> structure is set to <b>VT_I8</b>. The <b>hVal.QuadPart</b> member contains the time in binary coded decimal (BCD) form. See Remarks.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param punkState [in]

PPointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pPropVarTimecode</i> is not <b>VT_I8</b>.

</td>
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

When the asynchronous method completes, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the application must call <a href="/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns">IMFTimecodeTranslate::EndConvertTimecodeToHNS</a> to complete the asynchronous request.

The value of <i>pPropVarTimecode</i> is a 64-bit unsigned value typed as a <b>LONGLONG</b>. The upper <b>DWORD</b> contains the range. (A <i>range</i> is a continuous series of time codes.) The lower <b>DWORD</b> contains the time code in the form of a hexadecimal number <i>0xhhmmssff</i>,  where each 2-byte sequence is read as a decimal value.


```cpp
void CreateTimeCode(
    DWORD dwFrames,
    DWORD dwSeconds,
    DWORD dwMinutes,
    DWORD dwHours,
    DWORD dwRange,
    PROPVARIANT *pvar
    )
{
    ULONGLONG ullTimecode = ((ULONGLONG)dwRange) << 32;

    ullTimecode +=   dwFrames  % 10;
    ullTimecode += (( (ULONGLONG)dwFrames )  / 10) << 4;
    ullTimecode += (( (ULONGLONG)dwSeconds ) % 10) << 8;
    ullTimecode += (( (ULONGLONG)dwSeconds ) / 10) << 12;
    ullTimecode += (( (ULONGLONG)dwMinutes ) % 10) << 16;
    ullTimecode += (( (ULONGLONG)dwMinutes ) / 10) << 20;
    ullTimecode += (( (ULONGLONG)dwHours )   % 10) << 24;
    ullTimecode += (( (ULONGLONG)dwHours )   / 10) << 28;

    pvar->vt = VT_I8;
    pvar->hVal.QuadPart = (LONGLONG)ullTimecode;
}

```

## -see-also

<a href="/windows/desktop/medfound/calling-asynchronous-methods">Calling Asynchronous Methods</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate">IMFTimecodeTranslate</a>