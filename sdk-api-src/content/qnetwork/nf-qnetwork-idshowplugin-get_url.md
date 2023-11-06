---
UID: NF:qnetwork.IDShowPlugin.get_URL
title: IDShowPlugin::get_URL (qnetwork.h)
description: The get_URL method retrieves the URL of the current web page.
helpviewer_keywords: ["IDShowPlugin interface [DirectShow]","get_URL method","IDShowPlugin.get_URL","IDShowPlugin::get_URL","IDShowPluginget_URL","dshow.idshowplugin_get_url","get_URL","get_URL method [DirectShow]","get_URL method [DirectShow]","IDShowPlugin interface","qnetwork/IDShowPlugin::get_URL"]
old-location: dshow\idshowplugin_get_url.htm
tech.root: dshow
ms.assetid: df1a2643-c89e-4edf-bd85-bce1c410d6cd
ms.date: 4/26/2023
ms.keywords: IDShowPlugin interface [DirectShow],get_URL method, IDShowPlugin.get_URL, IDShowPlugin::get_URL, IDShowPluginget_URL, dshow.idshowplugin_get_url, get_URL, get_URL method [DirectShow], get_URL method [DirectShow],IDShowPlugin interface, qnetwork/IDShowPlugin::get_URL
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IDShowPlugin::get_URL
 - qnetwork/IDShowPlugin::get_URL
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
 - IDShowPlugin.get_URL
---

# IDShowPlugin::get_URL


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_URL</b> method retrieves the URL of the current web page.

## -parameters

### -param pURL

Receives the URL.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b>, by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-idshowplugin">IDShowPlugin Interface</a>