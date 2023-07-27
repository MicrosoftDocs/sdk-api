---
UID: NF:qnetwork.IAMMediaContent.get_BaseURL
title: IAMMediaContent::get_BaseURL (qnetwork.h)
description: The get_BaseURL method gets a base URL for the related web content.
helpviewer_keywords: ["IAMMediaContent interface [DirectShow]","get_BaseURL method","IAMMediaContent.get_BaseURL","IAMMediaContent::get_BaseURL","IAMMediaContentget_BaseURL","dshow.iammediacontent_get_baseurl","get_BaseURL","get_BaseURL method [DirectShow]","get_BaseURL method [DirectShow]","IAMMediaContent interface","qnetwork/IAMMediaContent::get_BaseURL"]
old-location: dshow\iammediacontent_get_baseurl.htm
tech.root: dshow
ms.assetid: 0fd88d09-79bf-45c6-93b4-1f57752ed1cd
ms.date: 4/26/2023
ms.keywords: IAMMediaContent interface [DirectShow],get_BaseURL method, IAMMediaContent.get_BaseURL, IAMMediaContent::get_BaseURL, IAMMediaContentget_BaseURL, dshow.iammediacontent_get_baseurl, get_BaseURL, get_BaseURL method [DirectShow], get_BaseURL method [DirectShow],IAMMediaContent interface, qnetwork/IAMMediaContent::get_BaseURL
req.header: qnetwork.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaContent::get_BaseURL
 - qnetwork/IAMMediaContent::get_BaseURL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMMediaContent.get_BaseURL
---

# IAMMediaContent::get_BaseURL


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_BaseURL</b> method gets a base URL for the related web content.

## -parameters

### -param pbstrBaseURL

Receives a <b>BSTR</b> with the information.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.
          

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

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
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Item not found.

</td>
</tr>
</table>

## -remarks

If the method succeeds, the caller must free the returned <b>BSTR</b> by calling the <b>SysFreeString</b> function.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iammediacontent">IAMMediaContent Interface</a>