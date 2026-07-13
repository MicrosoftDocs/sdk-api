---
UID: NF:mfmediaengine.IMFMediaEngine.Load
title: IMFMediaEngine::Load (mfmediaengine.h)
description: Loads the current media source.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","Load method","IMFMediaEngine.Load","IMFMediaEngine::Load","Load","Load method [Media Foundation]","Load method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_load","mfmediaengine/IMFMediaEngine::Load"]
old-location: mf\imfmediaengine_load.htm
tech.root: mf
ms.assetid: 5ACE8143-DC14-495C-A644-A2076FB1980F
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],Load method, IMFMediaEngine.Load, IMFMediaEngine::Load, Load, Load method [Media Foundation], Load method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_load, mfmediaengine/IMFMediaEngine::Load
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
 - IMFMediaEngine::Load
 - mfmediaengine/IMFMediaEngine::Load
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
 - IMFMediaEngine.Load
---

# IMFMediaEngine::Load


## -description

Loads the current media source.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The main purpose of this method is to reload a list of source elements after updating the list. For more information, see <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsourceelements">SetSourceElements</a>. Otherwise, calling this method is generally not required. To load a new media source, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">IMFMediaEngine::SetSource</a> or <b>IMFMediaEngine::SetSourceElements</b>.

The <b>Load</b> method explicitly invokes the Media Engine's media resource loading algorithm. Before calling this method, you must set the media resource by calling <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">IMFMediaEngine::SetSource</a> or <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsourceelements">IMFMediaEngine::SetSourceElements</a>. 

This method completes asynchronously. When the <b>Load</b> operation starts, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_LOADSTART</b> event. If no errors occur during the <b>Load</b> operation, several other events are generated, including the following.

<ul>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDMETADATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDDATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAY</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAYTHROUGH</b></li>
</ul>
If the Media Engine is unable to load the file, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_ERROR</b> event. 

For more information about event handling in the Media Engine, see <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify">IMFMediaEngineNotify</a>.

This method corresponds to the <b>load</b> method of the <b>HTMLMediaElement</b> interface in HTML5.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
