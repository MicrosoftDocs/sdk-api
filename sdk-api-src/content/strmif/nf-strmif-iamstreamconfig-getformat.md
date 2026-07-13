---
UID: NF:strmif.IAMStreamConfig.GetFormat
title: IAMStreamConfig::GetFormat (strmif.h)
description: The GetFormat method retrieves the current or preferred output format.
helpviewer_keywords: ["GetFormat","GetFormat method [DirectShow]","GetFormat method [DirectShow]","IAMStreamConfig interface","IAMStreamConfig interface [DirectShow]","GetFormat method","IAMStreamConfig.GetFormat","IAMStreamConfig::GetFormat","IAMStreamConfigGetFormat","dshow.iamstreamconfig_getformat","strmif/IAMStreamConfig::GetFormat"]
old-location: dshow\iamstreamconfig_getformat.htm
tech.root: dshow
ms.assetid: 5443141b-eb2c-412c-8bd1-7175e724b602
ms.date: 4/26/2023
ms.keywords: GetFormat, GetFormat method [DirectShow], GetFormat method [DirectShow],IAMStreamConfig interface, IAMStreamConfig interface [DirectShow],GetFormat method, IAMStreamConfig.GetFormat, IAMStreamConfig::GetFormat, IAMStreamConfigGetFormat, dshow.iamstreamconfig_getformat, strmif/IAMStreamConfig::GetFormat
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
 - IAMStreamConfig::GetFormat
 - strmif/IAMStreamConfig::GetFormat
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
 - IAMStreamConfig.GetFormat
---

# IAMStreamConfig::GetFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetFormat</code> method retrieves the current or preferred output format.

## -parameters

### -param ppmt [out]

Address of a pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure.

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
<b>NULL</b> pointer value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The input pin is not connected.

</td>
</tr>
</table>

## -remarks

If the pin is connected, this method returns the format that the pin is currently using. Otherwise, the method returns the pin's preferred format for the next pin connection. If you have already called the <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamconfig-setformat">IAMStreamConfig::SetFormat</a> method to set the format, <code>GetFormat</code> returns the same format. If not, it returns the first format in the pin's list of preferred formats, as determined by the <a href="/windows/desktop/api/strmif/nf-strmif-ipin-enummediatypes">IPin::EnumMediaTypes</a> method.

The method allocates the memory for the <b>AM_MEDIA_TYPE</b> structure, fills in the structure, and returns it in the <i>pmt</i> parameter. The caller must release the memory, including the format block. You can use the <a href="/windows/desktop/DirectShow/deletemediatype">DeleteMediaType</a> helper function in the base class library.

On some compression filters, the method fails if the filter's input pin is not connected.


#### Examples

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IAMStreamConfig *pConfig = NULL;
// Query the output pin for IAMStreamConfig (not shown).
AM_MEDIA_TYPE *pmt = NULL;
hr = pConfig-&gt;GetFormat(&amp;pmt);
if (SUCCEEDED(hr))
{
    /* Examine the media type for any information you need. */
    DeleteMediaType(pmt);
}
pConfig-&gt;Release();
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamstreamconfig">IAMStreamConfig Interface</a>