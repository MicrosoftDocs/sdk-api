---
UID: NF:control.IAMStats.GetValueByIndex
title: IAMStats::GetValueByIndex (control.h)
description: The GetValueByIndex method retrieves a statistic, by index.
helpviewer_keywords: ["GetValueByIndex","GetValueByIndex method [DirectShow]","GetValueByIndex method [DirectShow]","IAMStats interface","IAMStats interface [DirectShow]","GetValueByIndex method","IAMStats.GetValueByIndex","IAMStats::GetValueByIndex","IAMStatsGetValueByIndex","control/IAMStats::GetValueByIndex","dshow.iamstats_getvaluebyindex"]
old-location: dshow\iamstats_getvaluebyindex.htm
tech.root: DirectShow
ms.assetid: 68a74f56-288b-4e7e-bb0d-a38d43e08c27
ms.date: 4/26/2023
ms.keywords: GetValueByIndex, GetValueByIndex method [DirectShow], GetValueByIndex method [DirectShow],IAMStats interface, IAMStats interface [DirectShow],GetValueByIndex method, IAMStats.GetValueByIndex, IAMStats::GetValueByIndex, IAMStatsGetValueByIndex, control/IAMStats::GetValueByIndex, dshow.iamstats_getvaluebyindex
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMStats::GetValueByIndex
 - control/IAMStats::GetValueByIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMStats.GetValueByIndex
---

# IAMStats::GetValueByIndex


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetValueByIndex</code> method retrieves a statistic, by index.

## -parameters

### -param lIndex [in]

Zero-based index of the statistic.

### -param szName [out]

Pointer to a variable that receives the name of the statistic.

### -param lCount [out]

Pointer to a variable that receives the number of values that were recorded.

### -param dLast [out]

Pointer to a variable that receives the most recent value that was recorded.

### -param dAverage [out]

Pointer to a variable that receives the average value.

### -param dStdDev [out]

Pointer to a variable that receives the standard deviation of the values. If the count is less than two, the standard deviation is zero.

### -param dMin [out]

Pointer to a variable that receives the minimum value that was recorded.

### -param dMax [out]

Pointer to a variable that receives the maximum value that was recorded.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

The caller must free the string returned in <i>szName</i>, by calling the <b>SysFreeString</b> function.

To get the number of statistics, call [IAMStats::GetIndex](/windows/desktop/api/control/nf-control-iamstats-getindex).

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-iamstats">IAMStats Interface</a>