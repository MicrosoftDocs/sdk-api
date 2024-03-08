---
UID: NF:strmif.IConfigAviMux.GetOutputCompatibilityIndex
title: IConfigAviMux::GetOutputCompatibilityIndex (strmif.h)
description: The GetOutputCompatibilityIndex method retrieves the setting for the AVI index format.
helpviewer_keywords: ["GetOutputCompatibilityIndex","GetOutputCompatibilityIndex method [DirectShow]","GetOutputCompatibilityIndex method [DirectShow]","IConfigAviMux interface","IConfigAviMux interface [DirectShow]","GetOutputCompatibilityIndex method","IConfigAviMux.GetOutputCompatibilityIndex","IConfigAviMux::GetOutputCompatibilityIndex","IConfigAviMuxGetOutputCompatibilityIndex","dshow.iconfigavimux_getoutputcompatibilityindex","strmif/IConfigAviMux::GetOutputCompatibilityIndex"]
old-location: dshow\iconfigavimux_getoutputcompatibilityindex.htm
tech.root: DirectShow
ms.assetid: 723f1662-4f1a-408b-a737-9095e7c14c4f
ms.date: 4/26/2023
ms.keywords: GetOutputCompatibilityIndex, GetOutputCompatibilityIndex method [DirectShow], GetOutputCompatibilityIndex method [DirectShow],IConfigAviMux interface, IConfigAviMux interface [DirectShow],GetOutputCompatibilityIndex method, IConfigAviMux.GetOutputCompatibilityIndex, IConfigAviMux::GetOutputCompatibilityIndex, IConfigAviMuxGetOutputCompatibilityIndex, dshow.iconfigavimux_getoutputcompatibilityindex, strmif/IConfigAviMux::GetOutputCompatibilityIndex
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
 - IConfigAviMux::GetOutputCompatibilityIndex
 - strmif/IConfigAviMux::GetOutputCompatibilityIndex
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
 - IConfigAviMux.GetOutputCompatibilityIndex
---

# IConfigAviMux::GetOutputCompatibilityIndex


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetOutputCompatibilityIndex</code> method retrieves the setting for the AVI index format.

## -parameters

### -param pfOldIndex [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Create an AVI 1.0 index, as well as an AVI 2.0 index.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Create an AVI 2.0 index, but not an AVI 1.0 index.</td>
</tr>
</table>

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

The AVI Mux filter always creates an AVI 2.0 index ('indx' format). If the value returned in <i>pfOldIndex</i> is <b>TRUE</b>, the AVI Mux also creates an AVI 1.0 index ('idx1' format), for backward compatibility with Video for Windows.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iconfigavimux">IConfigAviMux Interface</a>



[IConfigAviMux::SetOutputCompatibilityIndex](/windows/desktop/api/strmif/nf-strmif-iconfigavimux-setoutputcompatibilityindex)