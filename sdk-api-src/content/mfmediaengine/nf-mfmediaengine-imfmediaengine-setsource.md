---
UID: NF:mfmediaengine.IMFMediaEngine.SetSource
title: IMFMediaEngine::SetSource (mfmediaengine.h)
description: Sets the URL of a media resource.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","SetSource method","IMFMediaEngine.SetSource","IMFMediaEngine::SetSource","SetSource","SetSource method [Media Foundation]","SetSource method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_setsource","mfmediaengine/IMFMediaEngine::SetSource"]
old-location: mf\imfmediaengine_setsource.htm
tech.root: mf
ms.assetid: 80C41EAB-9B8F-4723-A4A7-A17F56FF5773
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetSource method, IMFMediaEngine.SetSource, IMFMediaEngine::SetSource, SetSource, SetSource method [Media Foundation], SetSource method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setsource, mfmediaengine/IMFMediaEngine::SetSource
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngine::SetSource
 - mfmediaengine/IMFMediaEngine::SetSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.SetSource
---

# IMFMediaEngine::SetSource


## -description

Sets the URL of a media resource.

## -parameters

### -param pUrl [in]

The URL of the media resource.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to setting the <b>src</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

The URL specified by this method takes precedence over media resources specified in the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsourceelements">IMFMediaEngine::SetSourceElements</a> method. To load the URL, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">IMFMediaEngine::Load</a>.

This method asynchronously loads the URL. When the operation starts, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_LOADSTART</b> event. If no errors occur during the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a> operation, several other events are generated, including the following.

<ul>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDMETADATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDDATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAY</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAYTHROUGH</b></li>
</ul>
If the Media Engine is unable to load the URL, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_ERROR</b> event. 

For more information about event handling in the Media Engine, see <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify">IMFMediaEngineNotify</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>