---
UID: NF:strmif.IPersistMediaPropertyBag.Load
title: IPersistMediaPropertyBag::Load (strmif.h)
description: The Load method loads properties from the media property bag into the filter.
helpviewer_keywords: ["IPersistMediaPropertyBag interface [DirectShow]","Load method","IPersistMediaPropertyBag.Load","IPersistMediaPropertyBag::Load","IPersistMediaPropertyBagLoad","Load","Load method [DirectShow]","Load method [DirectShow]","IPersistMediaPropertyBag interface","dshow.ipersistmediapropertybag_load","strmif/IPersistMediaPropertyBag::Load"]
old-location: dshow\ipersistmediapropertybag_load.htm
tech.root: dshow
ms.assetid: 02ee3911-0b85-404d-81c9-7d0e6b3ccd5d
ms.date: 4/26/2023
ms.keywords: IPersistMediaPropertyBag interface [DirectShow],Load method, IPersistMediaPropertyBag.Load, IPersistMediaPropertyBag::Load, IPersistMediaPropertyBagLoad, Load, Load method [DirectShow], Load method [DirectShow],IPersistMediaPropertyBag interface, dshow.ipersistmediapropertybag_load, strmif/IPersistMediaPropertyBag::Load
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
 - IPersistMediaPropertyBag::Load
 - strmif/IPersistMediaPropertyBag::Load
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
 - IPersistMediaPropertyBag.Load
---

# IPersistMediaPropertyBag::Load


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Load</code> method loads properties from the media property bag into the filter.

## -parameters

### -param pPropBag [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-imediapropertybag">IMediaPropertyBag</a> interface of a media property bag created by the caller.

### -param pErrorLog [in]

Reserved. Set the value to <b>NULL</b>.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following:

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
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Access denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Filter graph is not in a stopped state.

</td>
</tr>
</table>

## -remarks

Call this method on the <a href="/windows/desktop/DirectShow/avi-mux-filter">AVI Mux</a> filter to write the properties into the AVI stream. Call the method when the filter is stopped, before you run the filter graph to author the file. When the graph runs, the filter writes the INFO chunks into the AVI header.

The following code example adds an IART (author name) INFO chunk to a file:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IPersistMediaPropertyBag *pPersist = NULL;
IMediaPropertyBag *pBag = NULL;
VARIANT val;

// Query the AVI Mux filter for IPersistMediaPropertyBag (not shown).

CoCreateInstance(CLSID_MediaPropertyBag, NULL, CLSCTX_INPROC,
        IID_IMediaPropertyBag, (LPVOID *)&amp;pBag);

val.vt = VT_BSTR;
val.bstrVal = SysAllocString(OLESTR("Author Name"));
pBag-&gt;Write(OLESTR("INFO/IART"), &amp;val);
pPersist-&gt;Load(pBag, NULL);
VariantClear(&amp;val);
</pre>
</td>
</tr>
</table></span></div>
The <a href="/windows/desktop/DirectShow/avi-splitter-filter">AVI Splitter</a> filter and the <a href="/windows/desktop/DirectShow/wave-parser-filter">WAVE Parser</a> do not support this method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipersistmediapropertybag">IPersistMediaPropertyBag Interface</a>