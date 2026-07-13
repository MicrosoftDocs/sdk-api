---
UID: NF:strmif.IResourceConsumer.AcquireResource
title: IResourceConsumer::AcquireResource (strmif.h)
description: The AcquireResource method notifies the resource consumer that a resource might be acquired.
helpviewer_keywords: ["AcquireResource","AcquireResource method [DirectShow]","AcquireResource method [DirectShow]","IResourceConsumer interface","IResourceConsumer interface [DirectShow]","AcquireResource method","IResourceConsumer.AcquireResource","IResourceConsumer::AcquireResource","IResourceConsumerAcquireResource","dshow.iresourceconsumer_acquireresource","strmif/IResourceConsumer::AcquireResource"]
old-location: dshow\iresourceconsumer_acquireresource.htm
tech.root: dshow
ms.assetid: e88d90af-681e-483b-9b29-9844eec75e41
ms.date: 4/26/2023
ms.keywords: AcquireResource, AcquireResource method [DirectShow], AcquireResource method [DirectShow],IResourceConsumer interface, IResourceConsumer interface [DirectShow],AcquireResource method, IResourceConsumer.AcquireResource, IResourceConsumer::AcquireResource, IResourceConsumerAcquireResource, dshow.iresourceconsumer_acquireresource, strmif/IResourceConsumer::AcquireResource
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IResourceConsumer::AcquireResource
 - strmif/IResourceConsumer::AcquireResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IResourceConsumer.AcquireResource
---

# IResourceConsumer::AcquireResource


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AcquireResource</code> method notifies the resource consumer that a resource might be acquired.

## -parameters

### -param idResource [in]

Resource identifier of the resource to be acquired.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Consumer has successfully acquired the resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Consumer has not acquired the resource but will use <a href="/windows/desktop/api/strmif/nf-strmif-iresourcemanager-notifyacquire">IResourceManager::NotifyAcquire</a> when it does.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_RESOURCE_NOT_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
Consumer no longer needs the resource.

</td>
</tr>
</table>
 

The method may return some other error code, if the consumer fails to acquire the resource.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iresourceconsumer">IResourceConsumer Interface</a>