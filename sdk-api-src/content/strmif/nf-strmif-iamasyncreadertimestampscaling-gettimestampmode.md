---
UID: NF:strmif.IAMAsyncReaderTimestampScaling.GetTimestampMode
title: IAMAsyncReaderTimestampScaling::GetTimestampMode (strmif.h)
description: Gets the filter's time-stamping mode.
helpviewer_keywords: ["FALSE","GetTimestampMode","GetTimestampMode method [DirectShow]","GetTimestampMode method [DirectShow]","IAMAsyncReaderTimestampScaling interface","IAMAsyncReaderTimestampScaling interface [DirectShow]","GetTimestampMode method","IAMAsyncReaderTimestampScaling.GetTimestampMode","IAMAsyncReaderTimestampScaling::GetTimestampMode","TRUE","dshow.iamasyncreadertimestampscaling_gettimestampmode","strmif/IAMAsyncReaderTimestampScaling::GetTimestampMode"]
old-location: dshow\iamasyncreadertimestampscaling_gettimestampmode.htm
tech.root: dshow
ms.assetid: 2fbadd9d-e741-482f-9ff1-655b149fec49
ms.date: 12/05/2018
ms.keywords: FALSE, GetTimestampMode, GetTimestampMode method [DirectShow], GetTimestampMode method [DirectShow],IAMAsyncReaderTimestampScaling interface, IAMAsyncReaderTimestampScaling interface [DirectShow],GetTimestampMode method, IAMAsyncReaderTimestampScaling.GetTimestampMode, IAMAsyncReaderTimestampScaling::GetTimestampMode, TRUE, dshow.iamasyncreadertimestampscaling_gettimestampmode, strmif/IAMAsyncReaderTimestampScaling::GetTimestampMode
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMAsyncReaderTimestampScaling::GetTimestampMode
 - strmif/IAMAsyncReaderTimestampScaling::GetTimestampMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMAsyncReaderTimestampScaling.GetTimestampMode
---

# IAMAsyncReaderTimestampScaling::GetTimestampMode


## -description

Gets the filter's time-stamping mode.

## -parameters

### -param pfRaw [out]

Receives a Boolean value.

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
Time stamps are in units of bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Time stamps are in units of bytes × 10000000. To get the offset in bytes, divide the sample time by 10000000.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamasyncreadertimestampscaling">IAMAsyncReaderTimestampScaling</a>