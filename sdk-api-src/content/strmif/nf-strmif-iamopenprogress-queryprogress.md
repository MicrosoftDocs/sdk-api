---
UID: NF:strmif.IAMOpenProgress.QueryProgress
title: IAMOpenProgress::QueryProgress (strmif.h)
description: The QueryProgress method retrieves the progress of the file-open operation.
helpviewer_keywords: ["IAMOpenProgress interface [DirectShow]","QueryProgress method","IAMOpenProgress.QueryProgress","IAMOpenProgress::QueryProgress","IAMOpenProgressQueryProgress","QueryProgress","QueryProgress method [DirectShow]","QueryProgress method [DirectShow]","IAMOpenProgress interface","dshow.iamopenprogress_queryprogress","strmif/IAMOpenProgress::QueryProgress"]
old-location: dshow\iamopenprogress_queryprogress.htm
tech.root: dshow
ms.assetid: 8471271d-36cc-4660-8a4e-4c234ba6b406
ms.date: 4/26/2023
ms.keywords: IAMOpenProgress interface [DirectShow],QueryProgress method, IAMOpenProgress.QueryProgress, IAMOpenProgress::QueryProgress, IAMOpenProgressQueryProgress, QueryProgress, QueryProgress method [DirectShow], QueryProgress method [DirectShow],IAMOpenProgress interface, dshow.iamopenprogress_queryprogress, strmif/IAMOpenProgress::QueryProgress
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
 - IAMOpenProgress::QueryProgress
 - strmif/IAMOpenProgress::QueryProgress
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
 - IAMOpenProgress.QueryProgress
---

# IAMOpenProgress::QueryProgress


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>QueryProgress</code> method retrieves the progress of the file-open operation.

## -parameters

### -param pllTotal [out]

Pointer to a variable that receives the length of the entire file, in bytes.

### -param pllCurrent [out]

Pointer to a variable that receives the length of the downloaded portion of the file, in bytes.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
<dt><b>VFW_S_ESTIMATED</b></dt>
</dl>
</td>
<td width="60%">
The returned values are estimates.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamopenprogress">IAMOpenProgress Interface</a>