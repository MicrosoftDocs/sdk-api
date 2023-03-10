---
UID: NF:mfidl.IMFByteStreamTimeSeek.GetTimeSeekResult
title: IMFByteStreamTimeSeek::GetTimeSeekResult (mfidl.h)
description: Gets the result of a time-based seek.
helpviewer_keywords: ["GetTimeSeekResult","GetTimeSeekResult method [Media Foundation]","GetTimeSeekResult method [Media Foundation]","IMFByteStreamTimeSeek interface","IMFByteStreamTimeSeek interface [Media Foundation]","GetTimeSeekResult method","IMFByteStreamTimeSeek.GetTimeSeekResult","IMFByteStreamTimeSeek::GetTimeSeekResult","mf.imfbytestreamtimeseek_gettimeseekresult","mfidl/IMFByteStreamTimeSeek::GetTimeSeekResult"]
old-location: mf\imfbytestreamtimeseek_gettimeseekresult.htm
tech.root: mf
ms.assetid: D56E1F06-AA05-430C-BF5C-30B38831B842
ms.date: 12/05/2018
ms.keywords: GetTimeSeekResult, GetTimeSeekResult method [Media Foundation], GetTimeSeekResult method [Media Foundation],IMFByteStreamTimeSeek interface, IMFByteStreamTimeSeek interface [Media Foundation],GetTimeSeekResult method, IMFByteStreamTimeSeek.GetTimeSeekResult, IMFByteStreamTimeSeek::GetTimeSeekResult, mf.imfbytestreamtimeseek_gettimeseekresult, mfidl/IMFByteStreamTimeSeek::GetTimeSeekResult
req.header: mfidl.h
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
 - IMFByteStreamTimeSeek::GetTimeSeekResult
 - mfidl/IMFByteStreamTimeSeek::GetTimeSeekResult
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
 - IMFByteStreamTimeSeek.GetTimeSeekResult
---

# IMFByteStreamTimeSeek::GetTimeSeekResult


## -description

Gets the result of a time-based seek.

## -parameters

### -param pqwStartTime [out]

Receives the new position after the seek, in 100-nanosecond units.

### -param pqwStopTime [out]

Receives the stop time, in 100-nanosecond units. If the stop time is unknown, the value is zero.

### -param pqwDuration [out]

Receives the total duration of the file, in 100-nanosecond units. If the duration is unknown, the value is –1.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The byte stream does not support time-based seeking, or no data is available.

</td>
</tr>
</table>

## -remarks

This method returns the server response from a previous time-based seek. 

<div class="alert"><b>Note</b>  This method normally cannot be invoked until some data
    is read from the byte stream, because the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamtimeseek-timeseek">IMFByteStreamTimeSeek::TimeSeek</a>       method does not send a server request immediately.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamtimeseek">IMFByteStreamTimeSeek</a>