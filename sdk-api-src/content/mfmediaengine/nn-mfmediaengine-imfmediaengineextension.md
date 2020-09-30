---
UID: NN:mfmediaengine.IMFMediaEngineExtension
title: IMFMediaEngineExtension (mfmediaengine.h)
description: Enables an application to load media resources in the Media Engine.
helpviewer_keywords: ["IMFMediaEngineExtension","IMFMediaEngineExtension interface [Media Foundation]","IMFMediaEngineExtension interface [Media Foundation]","described","mf.imfmediaengineextension","mfmediaengine/IMFMediaEngineExtension"]
old-location: mf\imfmediaengineextension.htm
tech.root: mf
ms.assetid: A032E0D0-2201-4B81-9FE0-8E9CE2707FDB
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineExtension, IMFMediaEngineExtension interface [Media Foundation], IMFMediaEngineExtension interface [Media Foundation],described, mf.imfmediaengineextension, mfmediaengine/IMFMediaEngineExtension
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
 - IMFMediaEngineExtension
 - mfmediaengine/IMFMediaEngineExtension
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
 - IMFMediaEngineExtension
---

# IMFMediaEngineExtension interface


## -description

Enables an application to load media resources in the Media Engine.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineExtension</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineExtension</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineExtension</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineextension-begincreateobject">BeginCreateObject</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request to create either a byte stream or a media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineextension-cancelobjectcreation">CancelObjectCreation</a>
</td>
<td align="left" width="63%">
Cancels the current request to create an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineextension-canplaytype">CanPlayType</a>
</td>
<td align="left" width="63%">
Queries whether the object can load a specified type of media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineextension-endcreateobject">EndCreateObject</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to create a byte stream or media source.

</td>
</tr>
</table>

## -remarks

To use this interface, set the <a href="/windows/desktop/medfound/mf-media-engine-extension">MF_MEDIA_ENGINE_EXTENSION</a> attribute when you call the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance">IMFMediaEngineClassFactory::CreateInstance</a> method.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>