---
UID: NF:qnetwork.IAMNetShowConfig.put_HTTPProxyHost
title: IAMNetShowConfig::put_HTTPProxyHost (qnetwork.h)
description: The put_HTTPProxyHost method specifies the address of the HTTP proxy server.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","put_HTTPProxyHost method","IAMNetShowConfig.put_HTTPProxyHost","IAMNetShowConfig::put_HTTPProxyHost","IAMNetShowConfigput_HTTPProxyHost","dshow.iamnetshowconfig_put_httpproxyhost","put_HTTPProxyHost","put_HTTPProxyHost method [DirectShow]","put_HTTPProxyHost method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::put_HTTPProxyHost"]
old-location: dshow\iamnetshowconfig_put_httpproxyhost.htm
tech.root: dshow
ms.assetid: 3cd37fd4-3ce0-4b5c-9e2f-88c0e1845b2d
ms.date: 4/26/2023
ms.keywords: IAMNetShowConfig interface [DirectShow],put_HTTPProxyHost method, IAMNetShowConfig.put_HTTPProxyHost, IAMNetShowConfig::put_HTTPProxyHost, IAMNetShowConfigput_HTTPProxyHost, dshow.iamnetshowconfig_put_httpproxyhost, put_HTTPProxyHost, put_HTTPProxyHost method [DirectShow], put_HTTPProxyHost method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_HTTPProxyHost
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
 - IAMNetShowConfig::put_HTTPProxyHost
 - qnetwork/IAMNetShowConfig::put_HTTPProxyHost
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
 - IAMNetShowConfig.put_HTTPProxyHost
---

# IAMNetShowConfig::put_HTTPProxyHost


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_HTTPProxyHost</code> method specifies the address of the HTTP proxy server.

## -parameters

### -param bstrHTTPProxyHost

Specifies the proxy's address.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-put_httpproxyport">IAMNetShowConfig::put_HTTPProxyPort</a>