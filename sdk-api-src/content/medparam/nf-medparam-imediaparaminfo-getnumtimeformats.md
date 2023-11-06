---
UID: NF:medparam.IMediaParamInfo.GetNumTimeFormats
title: IMediaParamInfo::GetNumTimeFormats (medparam.h)
description: The GetNumTimeFormats method retrieves the number of time formats that the object supports.
helpviewer_keywords: ["GetNumTimeFormats","GetNumTimeFormats method [DirectShow]","GetNumTimeFormats method [DirectShow]","IMediaParamInfo interface","IMediaParamInfo interface [DirectShow]","GetNumTimeFormats method","IMediaParamInfo.GetNumTimeFormats","IMediaParamInfo::GetNumTimeFormats","IMediaParamInfoGetNumTimeFormats","dshow.imediaparaminfo_getnumtimeformats","medparam/IMediaParamInfo::GetNumTimeFormats"]
old-location: dshow\imediaparaminfo_getnumtimeformats.htm
tech.root: dshow
ms.assetid: 5c398554-af2b-4e7d-8f5c-1c361535e7c6
ms.date: 4/26/2023
ms.keywords: GetNumTimeFormats, GetNumTimeFormats method [DirectShow], GetNumTimeFormats method [DirectShow],IMediaParamInfo interface, IMediaParamInfo interface [DirectShow],GetNumTimeFormats method, IMediaParamInfo.GetNumTimeFormats, IMediaParamInfo::GetNumTimeFormats, IMediaParamInfoGetNumTimeFormats, dshow.imediaparaminfo_getnumtimeformats, medparam/IMediaParamInfo::GetNumTimeFormats
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
 - IMediaParamInfo::GetNumTimeFormats
 - medparam/IMediaParamInfo::GetNumTimeFormats
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
 - IMediaParamInfo.GetNumTimeFormats
---

# IMediaParamInfo::GetNumTimeFormats


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetNumTimeFormats</code> method retrieves the number of time formats that the object supports.

## -parameters

### -param pdwNumTimeFormats [out]

Pointer to a variable that receives the number of supported time formats.

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

## -see-also

<a href="/windows/desktop/api/medparam/nn-medparam-imediaparaminfo">IMediaParamInfo Interface</a>