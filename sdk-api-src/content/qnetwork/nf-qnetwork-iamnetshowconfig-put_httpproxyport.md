---
UID: NF:qnetwork.IAMNetShowConfig.put_HTTPProxyPort
title: IAMNetShowConfig::put_HTTPProxyPort (qnetwork.h)
description: The put_HTTPProxyPort method specifies the port for the HTTP proxy server.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","put_HTTPProxyPort method","IAMNetShowConfig.put_HTTPProxyPort","IAMNetShowConfig::put_HTTPProxyPort","IAMNetShowConfigput_HTTPProxyPort","dshow.iamnetshowconfig_put_httpproxyport","put_HTTPProxyPort","put_HTTPProxyPort method [DirectShow]","put_HTTPProxyPort method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::put_HTTPProxyPort"]
old-location: dshow\iamnetshowconfig_put_httpproxyport.htm
tech.root: dshow
ms.assetid: dada8684-66e7-4983-984a-589d48d167ba
ms.date: 4/26/2023
ms.keywords: IAMNetShowConfig interface [DirectShow],put_HTTPProxyPort method, IAMNetShowConfig.put_HTTPProxyPort, IAMNetShowConfig::put_HTTPProxyPort, IAMNetShowConfigput_HTTPProxyPort, dshow.iamnetshowconfig_put_httpproxyport, put_HTTPProxyPort, put_HTTPProxyPort method [DirectShow], put_HTTPProxyPort method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_HTTPProxyPort
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
 - IAMNetShowConfig::put_HTTPProxyPort
 - qnetwork/IAMNetShowConfig::put_HTTPProxyPort
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
 - IAMNetShowConfig.put_HTTPProxyPort
---

# IAMNetShowConfig::put_HTTPProxyPort


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_HTTPProxyPort</code> method specifies the port for the HTTP proxy server.

## -parameters

### -param HTTPProxyPort

Specifies the HTTP proxy port.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-put_httpproxyhost">IAMNetShowConfig::put_HTTPProxyHost</a>