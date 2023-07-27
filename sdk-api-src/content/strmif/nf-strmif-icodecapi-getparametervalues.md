---
UID: NF:strmif.ICodecAPI.GetParameterValues
title: ICodecAPI::GetParameterValues (strmif.h)
description: The GetParameterValues method gets the list of possible values for a codec property. (ICodecAPI.GetParameterValues)
helpviewer_keywords: ["GetParameterValues","GetParameterValues method [DirectShow]","GetParameterValues method [DirectShow]","ICodecAPI interface","ICodecAPI interface [DirectShow]","GetParameterValues method","ICodecAPI.GetParameterValues","ICodecAPI::GetParameterValues","ICodecAPIGetParameterValues","dshow.icodecapi_getparametervalues","strmif/ICodecAPI::GetParameterValues"]
old-location: dshow\icodecapi_getparametervalues.htm
tech.root: dshow
ms.assetid: 7f6c7db8-f71f-4ea7-8584-0df6e28c0fc9
ms.date: 4/26/2023
ms.keywords: GetParameterValues, GetParameterValues method [DirectShow], GetParameterValues method [DirectShow],ICodecAPI interface, ICodecAPI interface [DirectShow],GetParameterValues method, ICodecAPI.GetParameterValues, ICodecAPI::GetParameterValues, ICodecAPIGetParameterValues, dshow.icodecapi_getparametervalues, strmif/ICodecAPI::GetParameterValues
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
 - ICodecAPI::GetParameterValues
 - strmif/ICodecAPI::GetParameterValues
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
 - ICodecAPI.GetParameterValues
---

# ICodecAPI::GetParameterValues


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetParameterValues</b> method gets the list of possible values for a codec property.

This method applies only to properties that support a list of possible values, as opposed to a linear range.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the property to query. For a list of standard codec properties, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

### -param Values [out]

Receives a pointer to an array of <b>VARIANT</b> types. The array contains the list of values that the encoder supports for this property. The caller must free each <b>VARIANT</b> by calling <b>VariantClear</b>. The caller must also free the array by calling  <b>CoTaskMemFree</b>.

### -param ValuesCount [out]

Receives the number of elements in the <i>Values</i> array.

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
<dt><b>VFW_E_CODECAPI_LINEAR_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The property supports a range of values, not a list.

</td>
</tr>
</table>

## -remarks

If the property supports a range of values, instead of a list, the method returns  <b>VFW_E_CODECAPI_LINEAR_RANGE</b>. In that case, call <a href="/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange">ICodecAPI::GetParameterRange</a> to get the range of values.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>
