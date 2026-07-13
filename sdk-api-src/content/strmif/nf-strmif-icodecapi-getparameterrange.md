---
UID: NF:strmif.ICodecAPI.GetParameterRange
title: ICodecAPI::GetParameterRange (strmif.h)
description: The GetParameterRange method gets the range of values for a codec property. (ICodecAPI.GetParameterRange)
helpviewer_keywords: ["GetParameterRange","GetParameterRange method [DirectShow]","GetParameterRange method [DirectShow]","ICodecAPI interface","ICodecAPI interface [DirectShow]","GetParameterRange method","ICodecAPI.GetParameterRange","ICodecAPI::GetParameterRange","ICodecAPIGetParameterRange","dshow.icodecapi_getparameterrange","strmif/ICodecAPI::GetParameterRange"]
old-location: dshow\icodecapi_getparameterrange.htm
tech.root: dshow
ms.assetid: 35bf758f-0ce3-4b3a-aae5-9d4326089743
ms.date: 4/26/2023
ms.keywords: GetParameterRange, GetParameterRange method [DirectShow], GetParameterRange method [DirectShow],ICodecAPI interface, ICodecAPI interface [DirectShow],GetParameterRange method, ICodecAPI.GetParameterRange, ICodecAPI::GetParameterRange, ICodecAPIGetParameterRange, dshow.icodecapi_getparameterrange, strmif/ICodecAPI::GetParameterRange
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
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
 - ICodecAPI::GetParameterRange
 - strmif/ICodecAPI::GetParameterRange
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
 - ICodecAPI.GetParameterRange
---

# ICodecAPI::GetParameterRange


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetParameterRange</b> method gets the range of values for a codec property. 
      

This method applies only to properties whose values form a linear range.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the property to query. For a list of standard codec properties, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

### -param ValueMin [out]

Pointer to a <b>VARIANT</b>  that receives the minimum value of the property. The caller must free the <b>VARIANT</b> by calling <b>VariantClear</b>.

### -param ValueMax [out]

Pointer to a <b>VARIANT</b>  that receives the maximum value of the property. The caller must free the <b>VARIANT</b> by calling <b>VariantClear</b>.

### -param SteppingDelta [out]

Pointer to a <b>VARIANT</b>  that receives the stepping delta, which defines the valid increments from <i>ValueMin</i> to <i>ValueMax</i>. The caller must free the <b>VARIANT</b> by calling <b>VariantClear</b>.

If the <b>VARIANT</b> type is VT_EMPTY, any increment is valid.

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
<dt><b>VFW_E_CODECAPI_ENUMERATED</b></dt>
</dl>
</td>
<td width="60%">
The property supports a list of possible values, not a linear range.

</td>
</tr>
</table>

## -remarks

The valid range for the property is [<i>ValueMin</i>... <i>ValueMax</i>], with increments of <i>SteppingDelta</i>. If a property supports a linear range of values, the property must use one of the following variant types:

<ul>
<li>Unsigned types: <b>VT_UI8</b>, <b>VT_UI4</b>, <b>VT_UI2</b>, <b>VT_UI1</b></li>
<li>Signed types: <b>VT_I8</b>, <b>VT_I4</b>, <b>VT_I2</b></li>
<li>Floating-point types: <b>VT_R8</b>, <b>VT_R4</b></li>
</ul>
If the property supports a list of values, instead of a range, the method returns  <b>VFW_E_CODECAPI_ENUMERATED</b>. In that case, call <a href="/windows/desktop/api/strmif/nf-strmif-icodecapi-getparametervalues">ICodecAPI::GetParameterValues</a> to get the list of values.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>
