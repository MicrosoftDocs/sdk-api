---
UID: NF:strmif.IAMVideoProcAmp.GetRange
title: IAMVideoProcAmp::GetRange (strmif.h)
description: The GetRange method gets the range and default value of a specified video property.
helpviewer_keywords: ["GetRange","GetRange method [DirectShow]","GetRange method [DirectShow]","IAMVideoProcAmp interface","IAMVideoProcAmp interface [DirectShow]","GetRange method","IAMVideoProcAmp.GetRange","IAMVideoProcAmp::GetRange","IAMVideoProcAmpGetRange","dshow.iamvideoprocamp_getrange","strmif/IAMVideoProcAmp::GetRange"]
old-location: dshow\iamvideoprocamp_getrange.htm
tech.root: dshow
ms.assetid: 54e462a8-bb65-43e2-acf1-f0d64db2bf24
ms.date: 4/26/2023
ms.keywords: GetRange, GetRange method [DirectShow], GetRange method [DirectShow],IAMVideoProcAmp interface, IAMVideoProcAmp interface [DirectShow],GetRange method, IAMVideoProcAmp.GetRange, IAMVideoProcAmp::GetRange, IAMVideoProcAmpGetRange, dshow.iamvideoprocamp_getrange, strmif/IAMVideoProcAmp::GetRange
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
 - IAMVideoProcAmp::GetRange
 - strmif/IAMVideoProcAmp::GetRange
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
 - IAMVideoProcAmp.GetRange
---

# IAMVideoProcAmp::GetRange


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetRange</code> method gets the range and default value of a specified video property.

## -parameters

### -param Property [in]

Specifies the property to query, as a value from the [VideoProcAmpProperty](/windows/desktop/api/strmif/ne-strmif-videoprocampproperty) enumeration.

### -param pMin [out]

Receives the minimum value of the property.

### -param pMax [out]

Receives the maximum value of the property.

### -param pSteppingDelta [out]

Receives the step size for the property. The step size is the smallest increment by which the property can change.

### -param pDefault [out]

Receives the default value of the property.

### -param pCapsFlags [out]

Receives one or more members of the [VideoProcAmpFlags](/windows/desktop/api/strmif/ne-strmif-videoprocampflags) enumeration, indicating whether the property is controlled automatically, manually, or both.

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
Invalid argument.

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
<dt><b>E_PROP_ID_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The device does not support this property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
No error.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideoprocamp">IAMVideoProcAmp Interface</a>
