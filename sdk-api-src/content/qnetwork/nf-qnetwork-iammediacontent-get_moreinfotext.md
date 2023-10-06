---
UID: NF:qnetwork.IAMMediaContent.get_MoreInfoText
title: IAMMediaContent::get_MoreInfoText (qnetwork.h)
description: The get_MoreInfoText method retrieves additional information as text.
helpviewer_keywords: ["IAMMediaContent interface [DirectShow]","get_MoreInfoText method","IAMMediaContent.get_MoreInfoText","IAMMediaContent::get_MoreInfoText","IAMMediaContentget_MoreInfoText","dshow.iammediacontent_get_moreinfotext","get_MoreInfoText","get_MoreInfoText method [DirectShow]","get_MoreInfoText method [DirectShow]","IAMMediaContent interface","qnetwork/IAMMediaContent::get_MoreInfoText"]
old-location: dshow\iammediacontent_get_moreinfotext.htm
tech.root: dshow
ms.assetid: 4a511c86-0a3a-48d3-8a3a-2ab52ff7dcea
ms.date: 4/26/2023
ms.keywords: IAMMediaContent interface [DirectShow],get_MoreInfoText method, IAMMediaContent.get_MoreInfoText, IAMMediaContent::get_MoreInfoText, IAMMediaContentget_MoreInfoText, dshow.iammediacontent_get_moreinfotext, get_MoreInfoText, get_MoreInfoText method [DirectShow], get_MoreInfoText method [DirectShow],IAMMediaContent interface, qnetwork/IAMMediaContent::get_MoreInfoText
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
 - IAMMediaContent::get_MoreInfoText
 - qnetwork/IAMMediaContent::get_MoreInfoText
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
 - IAMMediaContent.get_MoreInfoText
---

# IAMMediaContent::get_MoreInfoText


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_MoreInfoText</code> method retrieves additional information as text.

## -parameters

### -param pbstrMoreInfoText

Pointer to a variable that receives a <b>BSTR</b> with the information.

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