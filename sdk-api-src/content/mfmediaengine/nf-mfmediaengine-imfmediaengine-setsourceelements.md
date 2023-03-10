---
UID: NF:mfmediaengine.IMFMediaEngine.SetSourceElements
title: IMFMediaEngine::SetSourceElements (mfmediaengine.h)
description: Sets a list of media sources.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","SetSourceElements method","IMFMediaEngine.SetSourceElements","IMFMediaEngine::SetSourceElements","SetSourceElements","SetSourceElements method [Media Foundation]","SetSourceElements method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_setsourceelements","mfmediaengine/IMFMediaEngine::SetSourceElements"]
old-location: mf\imfmediaengine_setsourceelements.htm
tech.root: mf
ms.assetid: 7B1A1C43-A9BD-4DBF-B6A7-53BF9295CDAC
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetSourceElements method, IMFMediaEngine.SetSourceElements, IMFMediaEngine::SetSourceElements, SetSourceElements, SetSourceElements method [Media Foundation], SetSourceElements method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setsourceelements, mfmediaengine/IMFMediaEngine::SetSourceElements
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
 - IMFMediaEngine::SetSourceElements
 - mfmediaengine/IMFMediaEngine::SetSourceElements
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
 - IMFMediaEngine.SetSourceElements
---

# IMFMediaEngine::SetSourceElements


## -description

Sets a list of media sources.

## -parameters

### -param pSrcElements [in]

A pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements">IMFMediaEngineSrcElements</a> interface. The caller must implement this interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to adding a list of <b>source</b> elements to a media element in HTML5. 

The Media Engine tries to load each item in the <i>pSrcElements</i> list, until it finds one that loads successfully. After this method is called, the application can use the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements">IMFMediaEngineSrcElements</a> interface to update the list at any time. To reload the list, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">IMFMediaEngine::Load</a>.

This method completes asynchronously. When the operation starts, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_LOADSTART</b> event. If no errors occur during the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a> operation, several other events are generated, including the following.

<ul>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDMETADATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDDATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAY</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAYTHROUGH</b></li>
</ul>
If the Media Engine is unable to load a URL, it sends an <b>MF_MEDIA_ENGINE_EVENT_ERROR</b> event. 

For more information about event handling in the Media Engine, see <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify">IMFMediaEngineNotify</a>.

If the application also calls <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">IMFMediaEngine::SetSource</a>, the URL passed to <b>SetSource</b> takes precedence over the list given to <b>SetSourceElements</b>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>