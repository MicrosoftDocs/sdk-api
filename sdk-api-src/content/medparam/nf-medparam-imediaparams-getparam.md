---
UID: NF:medparam.IMediaParams.GetParam
title: IMediaParams::GetParam (medparam.h)
description: The GetParam method retrieves the current value of the specified parameter. If the parameter is currently within an envelope segment, the returned value is the value on the most recently processed sample.
helpviewer_keywords: ["GetParam","GetParam method [DirectShow]","GetParam method [DirectShow]","IMediaParams interface","IMediaParams interface [DirectShow]","GetParam method","IMediaParams.GetParam","IMediaParams::GetParam","IMediaParamsGetParam","dshow.imediaparams_getparam","medparam/IMediaParams::GetParam"]
old-location: dshow\imediaparams_getparam.htm
tech.root: dshow
ms.assetid: 4fcae36a-c659-4565-9169-66d97beb26a4
ms.date: 4/26/2023
ms.keywords: GetParam, GetParam method [DirectShow], GetParam method [DirectShow],IMediaParams interface, IMediaParams interface [DirectShow],GetParam method, IMediaParams.GetParam, IMediaParams::GetParam, IMediaParamsGetParam, dshow.imediaparams_getparam, medparam/IMediaParams::GetParam
req.header: medparam.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaParams::GetParam
 - medparam/IMediaParams::GetParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaParams.GetParam
---

# IMediaParams::GetParam


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetParam</code> method retrieves the current value of the specified parameter. If the parameter is currently within an envelope segment, the returned value is the value on the most recently processed sample.

## -parameters

### -param dwParamIndex [in]

Zero-based index of the parameter.

### -param pValue [out]

Pointer to a variable of type <b>MP_DATA</b> that receives the parameter value.

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

To enumerate the parameters supported by this object, along with their index values, use the <a href="/windows/desktop/api/medparam/nn-medparam-imediaparaminfo">IMediaParamInfo</a> interface.

## -see-also

<a href="/windows/desktop/api/medparam/nn-medparam-imediaparams">IMediaParams Interface</a>