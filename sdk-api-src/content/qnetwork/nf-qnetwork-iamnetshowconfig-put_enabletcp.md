---
UID: NF:qnetwork.IAMNetShowConfig.put_EnableTCP
title: IAMNetShowConfig::put_EnableTCP (qnetwork.h)
description: The put_EnableTCP method enables or disables TCP-based streaming.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","put_EnableTCP method","IAMNetShowConfig.put_EnableTCP","IAMNetShowConfig::put_EnableTCP","IAMNetShowConfigput_EnableTCP","dshow.iamnetshowconfig_put_enabletcp","put_EnableTCP","put_EnableTCP method [DirectShow]","put_EnableTCP method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::put_EnableTCP"]
old-location: dshow\iamnetshowconfig_put_enabletcp.htm
tech.root: dshow
ms.assetid: 8e875901-7ccb-4aa5-b283-f75b791e85f1
ms.date: 4/26/2023
ms.keywords: IAMNetShowConfig interface [DirectShow],put_EnableTCP method, IAMNetShowConfig.put_EnableTCP, IAMNetShowConfig::put_EnableTCP, IAMNetShowConfigput_EnableTCP, dshow.iamnetshowconfig_put_enabletcp, put_EnableTCP, put_EnableTCP method [DirectShow], put_EnableTCP method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_EnableTCP
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
 - IAMNetShowConfig::put_EnableTCP
 - qnetwork/IAMNetShowConfig::put_EnableTCP
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
 - IAMNetShowConfig.put_EnableTCP
---

# IAMNetShowConfig::put_EnableTCP


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_EnableTCP</code> method enables or disables TCP-based streaming.

## -parameters

### -param EnableTCP

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
<td>Enable TCP-based streaming.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Disable TCP-based streaming.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-put_enableudp">IAMNetShowConfig::put_EnableUDP</a>