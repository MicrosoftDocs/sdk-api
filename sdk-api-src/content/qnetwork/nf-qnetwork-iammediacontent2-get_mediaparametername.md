---
UID: NF:qnetwork.IAMMediaContent2.get_MediaParameterName
title: IAMMediaContent2::get_MediaParameterName (qnetwork.h)
description: The get_MediaParameterName method retrieves the name of a custom parameter in an ASX file.
helpviewer_keywords: ["IAMMediaContent2 interface [DirectShow]","get_MediaParameterName method","IAMMediaContent2.get_MediaParameterName","IAMMediaContent2::get_MediaParameterName","IAMMediaContent2get_MediaParameterName","dshow.iammediacontent2_get_mediaparametername","get_MediaParameterName","get_MediaParameterName method [DirectShow]","get_MediaParameterName method [DirectShow]","IAMMediaContent2 interface","qnetwork/IAMMediaContent2::get_MediaParameterName"]
old-location: dshow\iammediacontent2_get_mediaparametername.htm
tech.root: dshow
ms.assetid: 67eb8a01-312a-45ee-8da3-59a1f9f952ec
ms.date: 4/26/2023
ms.keywords: IAMMediaContent2 interface [DirectShow],get_MediaParameterName method, IAMMediaContent2.get_MediaParameterName, IAMMediaContent2::get_MediaParameterName, IAMMediaContent2get_MediaParameterName, dshow.iammediacontent2_get_mediaparametername, get_MediaParameterName, get_MediaParameterName method [DirectShow], get_MediaParameterName method [DirectShow],IAMMediaContent2 interface, qnetwork/IAMMediaContent2::get_MediaParameterName
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
 - IAMMediaContent2::get_MediaParameterName
 - qnetwork/IAMMediaContent2::get_MediaParameterName
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
 - IAMMediaContent2.get_MediaParameterName
---

# IAMMediaContent2::get_MediaParameterName


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_MediaParameterName</code> method retrieves the name of a custom parameter in an ASX file.



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

### -param Index

Specifies the index of the parameter to retrieve, indexed from 1.

### -param pbstrName

Pointer to a variable that receives the parameter name.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iammediacontent2">IAMMediaContent2 Interface</a>