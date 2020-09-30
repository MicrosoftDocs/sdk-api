---
UID: NN:mfmediaengine.IMFMediaEngineNotify
title: IMFMediaEngineNotify (mfmediaengine.h)
description: Callback interface for the IMFMediaEngine interface.
helpviewer_keywords: ["IMFMediaEngineNotify","IMFMediaEngineNotify interface [Media Foundation]","IMFMediaEngineNotify interface [Media Foundation]","described","mf.imfmediaenginenotify","mfmediaengine/IMFMediaEngineNotify"]
old-location: mf\imfmediaenginenotify.htm
tech.root: mf
ms.assetid: 85D702D4-3C9B-4848-81F2-3634C2B6AE1A
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineNotify, IMFMediaEngineNotify interface [Media Foundation], IMFMediaEngineNotify interface [Media Foundation],described, mf.imfmediaenginenotify, mfmediaengine/IMFMediaEngineNotify
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
 - IMFMediaEngineNotify
 - mfmediaengine/IMFMediaEngineNotify
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
 - IMFMediaEngineNotify
---

# IMFMediaEngineNotify interface


## -description

Callback interface for the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineNotify</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginenotify-eventnotify">EventNotify</a>
</td>
<td align="left" width="63%">
Notifies the application when a playback event occurs.

</td>
</tr>
</table>

## -remarks

To set the callback pointer on the Media Engine, set the <a href="/windows/desktop/medfound/mf-media-engine-callback">MF_MEDIA_ENGINE_CALLBACK</a> attribute in the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance">IMFMediaEngineClassFactory::CreateInstance</a> method.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>