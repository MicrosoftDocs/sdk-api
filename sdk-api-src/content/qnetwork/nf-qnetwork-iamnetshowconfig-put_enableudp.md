---
UID: NF:qnetwork.IAMNetShowConfig.put_EnableUDP
title: IAMNetShowConfig::put_EnableUDP (qnetwork.h)
description: The put_EnableUDP method enables or disables UDP-based streaming.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","put_EnableUDP method","IAMNetShowConfig.put_EnableUDP","IAMNetShowConfig::put_EnableUDP","IAMNetShowConfigput_EnableUDP","dshow.iamnetshowconfig_put_enableudp","put_EnableUDP","put_EnableUDP method [DirectShow]","put_EnableUDP method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::put_EnableUDP"]
old-location: dshow\iamnetshowconfig_put_enableudp.htm
tech.root: dshow
ms.assetid: 2573573e-97e0-4ed4-b702-8c54ef47c5f4
ms.date: 4/26/2023
ms.keywords: IAMNetShowConfig interface [DirectShow],put_EnableUDP method, IAMNetShowConfig.put_EnableUDP, IAMNetShowConfig::put_EnableUDP, IAMNetShowConfigput_EnableUDP, dshow.iamnetshowconfig_put_enableudp, put_EnableUDP, put_EnableUDP method [DirectShow], put_EnableUDP method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_EnableUDP
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
 - IAMNetShowConfig::put_EnableUDP
 - qnetwork/IAMNetShowConfig::put_EnableUDP
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
 - IAMNetShowConfig.put_EnableUDP
---

# IAMNetShowConfig::put_EnableUDP


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_EnableUDP</code> method enables or disables UDP-based streaming.

## -parameters

### -param EnableUDP

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
<td>Enable UDP-based streaming.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Disable UDP-based streaming.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-put_enabletcp">IAMNetShowConfig::put_EnableTCP</a>