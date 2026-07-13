---
UID: NF:strmif.IQualityControl.SetSink
title: IQualityControl::SetSink (strmif.h)
description: The SetSink method sets the IQualityControl object that will receive quality messages.
helpviewer_keywords: ["IQualityControl interface [DirectShow]","SetSink method","IQualityControl.SetSink","IQualityControl::SetSink","IQualityControlSetSink","SetSink","SetSink method [DirectShow]","SetSink method [DirectShow]","IQualityControl interface","dshow.iqualitycontrol_setsink","strmif/IQualityControl::SetSink"]
old-location: dshow\iqualitycontrol_setsink.htm
tech.root: dshow
ms.assetid: f82922dc-ec33-499d-b052-a1ba38632c52
ms.date: 4/26/2023
ms.keywords: IQualityControl interface [DirectShow],SetSink method, IQualityControl.SetSink, IQualityControl::SetSink, IQualityControlSetSink, SetSink, SetSink method [DirectShow], SetSink method [DirectShow],IQualityControl interface, dshow.iqualitycontrol_setsink, strmif/IQualityControl::SetSink
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
 - IQualityControl::SetSink
 - strmif/IQualityControl::SetSink
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
 - IQualityControl.SetSink
---

# IQualityControl::SetSink


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetSink</code> method sets the <a href="/windows/desktop/api/strmif/nn-strmif-iqualitycontrol">IQualityControl</a> object that will receive quality messages.

## -parameters

### -param piqc

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-iqualitycontrol">IQualityControl</a> object to which the notifications should be sent.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation. <b>HRESULT</b> can be one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method isn't supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK or NOERROR</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

The filter that receives a call to this method should record the <i>piqc</i> but should not add a reference count to it. The object pointed to will be a quality manager and will be a part of the filter graph (for example, a plug-in distributor). Adding a reference count to this could cause circular reference problems.

The reference to the object specified in <i>piqc</i> is guaranteed to be valid until this method is called with a null value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iqualitycontrol">IQualityControl Interface</a>