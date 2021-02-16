---
UID: NF:strmif.IMediaSeeking.GetPreroll
title: IMediaSeeking::GetPreroll (strmif.h)
description: The GetPreroll method retrieves the amount of data that will be queued before the start position.
helpviewer_keywords: ["GetPreroll","GetPreroll method [DirectShow]","GetPreroll method [DirectShow]","IMediaSeeking interface","IMediaSeeking interface [DirectShow]","GetPreroll method","IMediaSeeking.GetPreroll","IMediaSeeking::GetPreroll","IMediaSeekingGetPreroll","dshow.imediaseeking_getpreroll","strmif/IMediaSeeking::GetPreroll"]
old-location: dshow\imediaseeking_getpreroll.htm
tech.root: dshow
ms.assetid: 9d519aab-eb35-4a00-b6fe-23d734f969ae
ms.date: 12/05/2018
ms.keywords: GetPreroll, GetPreroll method [DirectShow], GetPreroll method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetPreroll method, IMediaSeeking.GetPreroll, IMediaSeeking::GetPreroll, IMediaSeekingGetPreroll, dshow.imediaseeking_getpreroll, strmif/IMediaSeeking::GetPreroll
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IMediaSeeking::GetPreroll
 - strmif/IMediaSeeking::GetPreroll
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
 - IMediaSeeking.GetPreroll
---

# IMediaSeeking::GetPreroll


## -description

The <code>GetPreroll</code> method retrieves the amount of data that will be queued before the start position.

## -parameters

### -param pllPreroll [out]

Pointer to a variable that receives the preroll time, in units of the current time format.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

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

The <i>preroll</i> is the time prior to the start position at which nonrandom access devices, such as tape players, should start rolling.

The returned value is expressed in the current time format. The default time format is <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> units (100 nanoseconds). To change time formats, use the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>