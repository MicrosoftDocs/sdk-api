---
UID: NF:mixerocx.IMixerOCXNotify.OnStatusChange
title: IMixerOCXNotify::OnStatusChange (mixerocx.h)
description: The OnStatusChange method informs the client that a status change has occurred.
helpviewer_keywords: ["IMixerOCXNotify interface [DirectShow]","OnStatusChange method","IMixerOCXNotify.OnStatusChange","IMixerOCXNotify::OnStatusChange","IMixerOCXNotifyOnStatusChange","OnStatusChange","OnStatusChange method [DirectShow]","OnStatusChange method [DirectShow]","IMixerOCXNotify interface","dshow.imixerocxnotify_onstatuschange","mixerocx/IMixerOCXNotify::OnStatusChange"]
old-location: dshow\imixerocxnotify_onstatuschange.htm
tech.root: dshow
ms.assetid: b6e49306-59bc-45a2-826b-cea2cf77214b
ms.date: 12/05/2018
ms.keywords: IMixerOCXNotify interface [DirectShow],OnStatusChange method, IMixerOCXNotify.OnStatusChange, IMixerOCXNotify::OnStatusChange, IMixerOCXNotifyOnStatusChange, OnStatusChange, OnStatusChange method [DirectShow], OnStatusChange method [DirectShow],IMixerOCXNotify interface, dshow.imixerocxnotify_onstatuschange, mixerocx/IMixerOCXNotify::OnStatusChange
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
 - IMixerOCXNotify::OnStatusChange
 - mixerocx/IMixerOCXNotify::OnStatusChange
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
 - IMixerOCXNotify.OnStatusChange
---

# IMixerOCXNotify::OnStatusChange


## -description

The <code>OnStatusChange</code> method informs the client that a status change has occurred.

## -parameters

### -param ulStatusFlags [in]

Bitwise OR of one or more of the following status flags.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>MIXER_STATE_UNCONNECTED (0x00000000)</td>
<td>The Overlay Mixer is unconnected and stopped.</td>
</tr>
<tr>
<td>MIXER_STATE_CONNECTED_STOPPED (0x00000001)</td>
<td>The Overlay Mixer is connected and stopped.</td>
</tr>
<tr>
<td>MIXER_STATE_CONNECTED_PAUSED (0x00000002)</td>
<td>The Overlay Mixer is connected and paused.</td>
</tr>
<tr>
<td>MIXER_STATE_CONNECTED_PLAYING (0x00000003)</td>
<td>The Overlay Mixer is connected and playing.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK.

## -see-also

<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify">IMixerOCXNotify Interface</a>



<a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>