---
UID: NF:strmif.IResourceManager.RequestResource
title: IResourceManager::RequestResource (strmif.h)
description: The RequestResource method requests the use of a given registered resource.
helpviewer_keywords: ["IResourceManager interface [DirectShow]","RequestResource method","IResourceManager.RequestResource","IResourceManager::RequestResource","IResourceManagerRequestResource","RequestResource","RequestResource method [DirectShow]","RequestResource method [DirectShow]","IResourceManager interface","dshow.iresourcemanager_requestresource","strmif/IResourceManager::RequestResource"]
old-location: dshow\iresourcemanager_requestresource.htm
tech.root: dshow
ms.assetid: b52dc38a-9246-4cef-ba1a-cf1927223183
ms.date: 4/26/2023
ms.keywords: IResourceManager interface [DirectShow],RequestResource method, IResourceManager.RequestResource, IResourceManager::RequestResource, IResourceManagerRequestResource, RequestResource, RequestResource method [DirectShow], RequestResource method [DirectShow],IResourceManager interface, dshow.iresourcemanager_requestresource, strmif/IResourceManager::RequestResource
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
 - IResourceManager::RequestResource
 - strmif/IResourceManager::RequestResource
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
 - IResourceManager.RequestResource
---

# IResourceManager::RequestResource


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>RequestResource</code> method requests the use of a given registered resource.

## -parameters

### -param idResource [in]

Resource token retrieved when the resource was registered.

### -param pFocusObject [in]

Pointer to the <b>IUnknown</b> interface of a focus object associated with a request (typically the <b>IUnknown</b> interface of the filter).

### -param pConsumer [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-iresourceconsumer">IResourceConsumer</a> interface on the object requesting the resource.

## -returns

Returns an <b>HRESULT</b> value. Returns S_OK if the requested resource is returned, or S_FALSE if the resource is not available, in which case the resource manager will call the requesting object back when the resource becomes available. Any other return is an error.

## -remarks

When there is more than one request for the resource, the resource manager will decide the priority by using the object of focus passed with each request and comparing it to the object of focus passed in the most recent <a href="/windows/desktop/api/strmif/nf-strmif-iresourcemanager-setfocus">IResourceManager::SetFocus</a> method.

Requests will be filled in the following order of priority:

<ol>
<li>Requests made with exactly the same object of focus as the last <a href="/windows/desktop/api/strmif/nf-strmif-iresourcemanager-setfocus">SetFocus</a> method.</li>
<li>Requests whose object of focus shares a common source filter whose object of focus shares a common filter graph.</li>
<li>Requests in the same process as the focus.</li>
</ol>
While checking this priority, the resource manager will use <b>QueryInterface</b> on the focus object for IID_IFilter. If found, the resource manager will use <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> methods to check the filter graph and look for common source filters with the current focus object.

A filter should pass the <b>IUnknown</b> interface of the filter in the <i>pFocusObject</i> parameter. The filter graph manager matches filters to the filter graph and will attempt to trace filters to common source filters when checking objects of focus.

The focus object must be valid for the entire lifetime of the request—until either the <a href="/windows/desktop/api/strmif/nf-strmif-iresourcemanager-cancelrequest">IResourceManager::CancelRequest</a> method is called, or the <a href="/windows/desktop/api/strmif/nf-strmif-iresourcemanager-notifyrelease">IResourceManager::NotifyRelease</a> method is called with the <i>bStillWant</i> parameter set to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iresourcemanager">IResourceManager Interface</a>