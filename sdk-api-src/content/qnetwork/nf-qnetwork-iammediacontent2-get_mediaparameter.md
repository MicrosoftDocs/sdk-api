---
UID: NF:qnetwork.IAMMediaContent2.get_MediaParameter
title: IAMMediaContent2::get_MediaParameter (qnetwork.h)
description: The get_MediaParameter method retrieves the value of a custom parameter in the ASX file.
helpviewer_keywords: ["IAMMediaContent2 interface [DirectShow]","get_MediaParameter method","IAMMediaContent2.get_MediaParameter","IAMMediaContent2::get_MediaParameter","IAMMediaContent2get_MediaParameter","dshow.iammediacontent2_get_mediaparameter","get_MediaParameter","get_MediaParameter method [DirectShow]","get_MediaParameter method [DirectShow]","IAMMediaContent2 interface","qnetwork/IAMMediaContent2::get_MediaParameter"]
old-location: dshow\iammediacontent2_get_mediaparameter.htm
tech.root: dshow
ms.assetid: 87e018bb-2073-46df-860a-c4de99a88189
ms.date: 4/26/2023
ms.keywords: IAMMediaContent2 interface [DirectShow],get_MediaParameter method, IAMMediaContent2.get_MediaParameter, IAMMediaContent2::get_MediaParameter, IAMMediaContent2get_MediaParameter, dshow.iammediacontent2_get_mediaparameter, get_MediaParameter, get_MediaParameter method [DirectShow], get_MediaParameter method [DirectShow],IAMMediaContent2 interface, qnetwork/IAMMediaContent2::get_MediaParameter
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
 - IAMMediaContent2::get_MediaParameter
 - qnetwork/IAMMediaContent2::get_MediaParameter
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
 - IAMMediaContent2.get_MediaParameter
---

# IAMMediaContent2::get_MediaParameter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_MediaParameter</code> method retrieves the value of a custom parameter in the ASX file.



This interface is not supported.

## -parameters

### -param EntryNum

Specifies the location of the parameter in the ASX file.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The parameter is a direct child of the ASX node.</td>
</tr>
<tr>
<td>&gt; 0</td>
<td>The parameter is located inside an ENTRY tag; <i>EntryNum</i> specifies the entry, indexed from 1.</td>
</tr>
</table>

### -param bstrName

Specifies the name of the parameter.

### -param pbstrValue

Pointer to a variable that receives the value of the parameter.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the <b>BSTR</b> returned in <i>pbstrValue</i>, by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iammediacontent2">IAMMediaContent2 Interface</a>