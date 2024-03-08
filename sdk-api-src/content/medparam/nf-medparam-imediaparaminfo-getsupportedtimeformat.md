---
UID: NF:medparam.IMediaParamInfo.GetSupportedTimeFormat
title: IMediaParamInfo::GetSupportedTimeFormat (medparam.h)
description: The GetSupportedTimeFormat method retrieves a supported time format.
helpviewer_keywords: ["GetSupportedTimeFormat","GetSupportedTimeFormat method [DirectShow]","GetSupportedTimeFormat method [DirectShow]","IMediaParamInfo interface","IMediaParamInfo interface [DirectShow]","GetSupportedTimeFormat method","IMediaParamInfo.GetSupportedTimeFormat","IMediaParamInfo::GetSupportedTimeFormat","IMediaParamInfoGetSupportedTimeFormat","dshow.imediaparaminfo_getsupportedtimeformat","medparam/IMediaParamInfo::GetSupportedTimeFormat"]
old-location: dshow\imediaparaminfo_getsupportedtimeformat.htm
tech.root: dshow
ms.assetid: 04e4c9ea-4570-4fd0-986b-c835c692b73b
ms.date: 4/26/2023
ms.keywords: GetSupportedTimeFormat, GetSupportedTimeFormat method [DirectShow], GetSupportedTimeFormat method [DirectShow],IMediaParamInfo interface, IMediaParamInfo interface [DirectShow],GetSupportedTimeFormat method, IMediaParamInfo.GetSupportedTimeFormat, IMediaParamInfo::GetSupportedTimeFormat, IMediaParamInfoGetSupportedTimeFormat, dshow.imediaparaminfo_getsupportedtimeformat, medparam/IMediaParamInfo::GetSupportedTimeFormat
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
 - IMediaParamInfo::GetSupportedTimeFormat
 - medparam/IMediaParamInfo::GetSupportedTimeFormat
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
 - IMediaParamInfo.GetSupportedTimeFormat
---

# IMediaParamInfo::GetSupportedTimeFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetSupportedTimeFormat</code> method retrieves a supported time format.

## -parameters

### -param dwFormatIndex [in]

Index of the time format to retrieve.

### -param pguidTimeFormat [out]

Pointer to a variable that receives a time format GUID.

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

Call the <a href="/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getnumtimeformats">GetNumTimeFormats</a> method to retrieve the number of time formats that the object supports.

## -see-also

<a href="/windows/desktop/api/medparam/nn-medparam-imediaparaminfo">IMediaParamInfo Interface</a>



<a href="/windows/desktop/DirectShow/time-format-guids">Time Format GUIDs</a>