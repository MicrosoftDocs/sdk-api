---
UID: NF:bdaiface.IEnumPIDMap.Skip
title: IEnumPIDMap::Skip (bdaiface.h)
description: The Skip method skips the specified number of elements in the collection.
helpviewer_keywords: ["IEnumPIDMap interface [DirectShow]","Skip method","IEnumPIDMap.Skip","IEnumPIDMap::Skip","IEnumPIDMapSkip","Skip","Skip method [DirectShow]","Skip method [DirectShow]","IEnumPIDMap interface","bdaiface/IEnumPIDMap::Skip","dshow.ienumpidmap_skip"]
old-location: dshow\ienumpidmap_skip.htm
tech.root: dshow
ms.assetid: e611e5a0-beb1-4a31-974a-29b2b8349a17
ms.date: 4/26/2023
ms.keywords: IEnumPIDMap interface [DirectShow],Skip method, IEnumPIDMap.Skip, IEnumPIDMap::Skip, IEnumPIDMapSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumPIDMap interface, bdaiface/IEnumPIDMap::Skip, dshow.ienumpidmap_skip
req.header: bdaiface.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumPIDMap::Skip
 - bdaiface/IEnumPIDMap::Skip
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
 - IEnumPIDMap.Skip
---

# IEnumPIDMap::Skip


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Skip</code> method skips the specified number of elements in the collection.

## -parameters

### -param cRecords [in]

Specifies the number of elements to skip.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Reached the end of the collection.

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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ienumpidmap">IEnumPIDMap Interface</a>