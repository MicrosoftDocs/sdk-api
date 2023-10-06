---
UID: NF:qnetwork.IDShowPlugin.get_UserAgent
title: IDShowPlugin::get_UserAgent (qnetwork.h)
description: The get_UserAgent method retrieves the User-Agent field from the HTTP header.
helpviewer_keywords: ["IDShowPlugin interface [DirectShow]","get_UserAgent method","IDShowPlugin.get_UserAgent","IDShowPlugin::get_UserAgent","IDShowPluginget_UserAgent","dshow.idshowplugin_get_useragent","get_UserAgent","get_UserAgent method [DirectShow]","get_UserAgent method [DirectShow]","IDShowPlugin interface","qnetwork/IDShowPlugin::get_UserAgent"]
old-location: dshow\idshowplugin_get_useragent.htm
tech.root: dshow
ms.assetid: 0bbd3cd2-75d8-4c48-837d-4cb045cad35b
ms.date: 4/26/2023
ms.keywords: IDShowPlugin interface [DirectShow],get_UserAgent method, IDShowPlugin.get_UserAgent, IDShowPlugin::get_UserAgent, IDShowPluginget_UserAgent, dshow.idshowplugin_get_useragent, get_UserAgent, get_UserAgent method [DirectShow], get_UserAgent method [DirectShow],IDShowPlugin interface, qnetwork/IDShowPlugin::get_UserAgent
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
 - IDShowPlugin::get_UserAgent
 - qnetwork/IDShowPlugin::get_UserAgent
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
 - IDShowPlugin.get_UserAgent
---

# IDShowPlugin::get_UserAgent


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_UserAgent</code> method retrieves the User-Agent field from the HTTP header.

## -parameters

### -param pUserAgent

Pointer to a variable that receives the User-Agent string.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b>, by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-idshowplugin">IDShowPlugin Interface</a>