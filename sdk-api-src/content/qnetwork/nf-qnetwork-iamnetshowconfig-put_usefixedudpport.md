---
UID: NF:qnetwork.IAMNetShowConfig.put_UseFixedUDPPort
title: IAMNetShowConfig::put_UseFixedUDPPort (qnetwork.h)
description: The put_UseFixedUDPPort method specifies whether to use a fixed UDP port number.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","put_UseFixedUDPPort method","IAMNetShowConfig.put_UseFixedUDPPort","IAMNetShowConfig::put_UseFixedUDPPort","IAMNetShowConfigput_UseFixedUDPPort","dshow.iamnetshowconfig_put_usefixedudpport","put_UseFixedUDPPort","put_UseFixedUDPPort method [DirectShow]","put_UseFixedUDPPort method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::put_UseFixedUDPPort"]
old-location: dshow\iamnetshowconfig_put_usefixedudpport.htm
tech.root: dshow
ms.assetid: a7b0c118-0479-4f28-8e2f-6c143cde9ff0
ms.date: 4/26/2023
ms.keywords: IAMNetShowConfig interface [DirectShow],put_UseFixedUDPPort method, IAMNetShowConfig.put_UseFixedUDPPort, IAMNetShowConfig::put_UseFixedUDPPort, IAMNetShowConfigput_UseFixedUDPPort, dshow.iamnetshowconfig_put_usefixedudpport, put_UseFixedUDPPort, put_UseFixedUDPPort method [DirectShow], put_UseFixedUDPPort method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_UseFixedUDPPort
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
 - IAMNetShowConfig::put_UseFixedUDPPort
 - qnetwork/IAMNetShowConfig::put_UseFixedUDPPort
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
 - IAMNetShowConfig.put_UseFixedUDPPort
---

# IAMNetShowConfig::put_UseFixedUDPPort


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_UseFixedUDPPort</code> method specifies whether to use a fixed UDP port number.

## -parameters

### -param UseFixedUDPPort

Specify one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Use a fixed UDP port.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Use a dynamic UDP port.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-put_fixedudpport">IAMNetShowConfig::put_FixedUDPPort</a>