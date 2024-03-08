---
UID: NF:medparam.IMediaParams.AddEnvelope
title: IMediaParams::AddEnvelope (medparam.h)
description: The AddEnvelope method adds an envelope to a parameter.
helpviewer_keywords: ["AddEnvelope","AddEnvelope method [DirectShow]","AddEnvelope method [DirectShow]","IMediaParams interface","IMediaParams interface [DirectShow]","AddEnvelope method","IMediaParams.AddEnvelope","IMediaParams::AddEnvelope","IMediaParamsAddEnvelope","dshow.imediaparams_addenvelope","medparam/IMediaParams::AddEnvelope"]
old-location: dshow\imediaparams_addenvelope.htm
tech.root: dshow
ms.assetid: acf7c96c-ce0c-40d0-b4a1-dd571fa2a514
ms.date: 4/26/2023
ms.keywords: AddEnvelope, AddEnvelope method [DirectShow], AddEnvelope method [DirectShow],IMediaParams interface, IMediaParams interface [DirectShow],AddEnvelope method, IMediaParams.AddEnvelope, IMediaParams::AddEnvelope, IMediaParamsAddEnvelope, dshow.imediaparams_addenvelope, medparam/IMediaParams::AddEnvelope
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
 - IMediaParams::AddEnvelope
 - medparam/IMediaParams::AddEnvelope
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
 - IMediaParams.AddEnvelope
---

# IMediaParams::AddEnvelope


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AddEnvelope</code> method adds an envelope to a parameter.

## -parameters

### -param dwParamIndex [in]

Zero-based index of the parameter, or DWORD_ALLPARAMS to add the envelope to every parameter.

### -param cSegments [in]

Number of segments in the envelope.

### -param pEnvelopeSegments [in]

Pointer to an array of <a href="/previous-versions/windows/desktop/api/medparam/ns-medparam-mp_envelope_segment">MP_ENVELOPE_SEGMENT</a> structures that define the envelope segments. The size of the array is given in the <i>cPoints</i> parameter.

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
<dt><b>E_OUTOFMEMEORY</b></dt>
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

The caller should add envelopes in time-ascending order. Otherwise, the results on playback are indeterminate. If one envelope overlaps another, the later envelope takes precedence.

To enumerate the parameters supported by this object, along with their index values, use the <a href="/windows/desktop/api/medparam/nn-medparam-imediaparaminfo">IMediaParamInfo</a> interface.


#### Examples

The following code sets two envelope segments, both using a linear function.


```cpp

#define MSEC 10000  // One millisecond

// Define an array with two segments. Note the segments appear in 
// time-ascending order.
MP_ENVELOPE_SEGMENT Segments[] =
{
    {  
        0,                  // rtStart
        3 * MSEC,           // rtStop
        0,                  // valStart
        12,                 // valStop
        MP_CURVE_LINEAR,    // iCurve
        MPF_ENVLP_STANDARD  // flags
    },
    {  
        6 * MSEC,
        9 * MSEC,
        12,
        0,
        MP_CURVE_LINEAR,
        MPF_ENVLP_STANDARD
    }
};
// Define the number of segments in the array.
DWORD cSegments = sizeof(Segments) / sizeof(Segments[0]);
DWORD dwParam = 0;  // Which parameter to set.

hr = pMediaParams->AddEnvelope(dwParam, cSegments, Segments);

```


This example assumes that the caller has previous used the <b>IMediaParamInfo</b> interface to query whether the DMO supports the MP_CURVE_LINEAR curve for that parameter.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/medparam/nn-medparam-imediaparams">IMediaParams Interface</a>