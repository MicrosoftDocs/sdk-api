---
UID: NF:mixerocx.IMixerOCXNotify.OnDataChange
title: IMixerOCXNotify::OnDataChange (mixerocx.h)
description: The OnDataChange method notifies the client when the video rectangle's aspect ratio or size, or the display palette, has changed.
helpviewer_keywords: ["IMixerOCXNotify interface [DirectShow]","OnDataChange method","IMixerOCXNotify.OnDataChange","IMixerOCXNotify::OnDataChange","IMixerOCXNotifyOnDataChange","OnDataChange","OnDataChange method [DirectShow]","OnDataChange method [DirectShow]","IMixerOCXNotify interface","dshow.imixerocxnotify_ondatachange","mixerocx/IMixerOCXNotify::OnDataChange"]
old-location: dshow\imixerocxnotify_ondatachange.htm
tech.root: dshow
ms.assetid: d8080e5f-99e7-47eb-96ff-53c4ed8d2ff1
ms.date: 12/05/2018
ms.keywords: IMixerOCXNotify interface [DirectShow],OnDataChange method, IMixerOCXNotify.OnDataChange, IMixerOCXNotify::OnDataChange, IMixerOCXNotifyOnDataChange, OnDataChange, OnDataChange method [DirectShow], OnDataChange method [DirectShow],IMixerOCXNotify interface, dshow.imixerocxnotify_ondatachange, mixerocx/IMixerOCXNotify::OnDataChange
req.header: mixerocx.h
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
 - IMixerOCXNotify::OnDataChange
 - mixerocx/IMixerOCXNotify::OnDataChange
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
 - IMixerOCXNotify.OnDataChange
---

# IMixerOCXNotify::OnDataChange


## -description

The <code>OnDataChange</code> method notifies the client when the video rectangle's aspect ratio or size, or the display palette, has changed.

## -parameters

### -param ulDataFlags [in]

Flag indicating which set of data has changed. The following flags are defined.

<table>
<tr>
<th>Flags
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>MIXER_DATA_ASPECT_RATIO (0x00000001)</td>
<td>Picture aspect ratio.</td>
</tr>
<tr>
<td>MIXER_DATA_NATIVE_SIZE (0x00000002)</td>
<td>The video stream's native size changed.</td>
</tr>
<tr>
<td>MIXER_DATA_PALETTE (0x00000004)</td>
<td>The video palette changed.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK.

## -see-also

<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify">IMixerOCXNotify Interface</a>