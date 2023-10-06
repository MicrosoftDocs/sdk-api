---
UID: NF:strmif.IResourceManager.CancelRequest
title: IResourceManager::CancelRequest (strmif.h)
description: The CancelRequest method cancels the request for a resource.
helpviewer_keywords: ["CancelRequest","CancelRequest method [DirectShow]","CancelRequest method [DirectShow]","IResourceManager interface","IResourceManager interface [DirectShow]","CancelRequest method","IResourceManager.CancelRequest","IResourceManager::CancelRequest","IResourceManagerCancelRequest","dshow.iresourcemanager_cancelrequest","strmif/IResourceManager::CancelRequest"]
old-location: dshow\iresourcemanager_cancelrequest.htm
tech.root: dshow
ms.assetid: 49372654-8e69-4a7a-915e-16e791c63fb2
ms.date: 4/26/2023
ms.keywords: CancelRequest, CancelRequest method [DirectShow], CancelRequest method [DirectShow],IResourceManager interface, IResourceManager interface [DirectShow],CancelRequest method, IResourceManager.CancelRequest, IResourceManager::CancelRequest, IResourceManagerCancelRequest, dshow.iresourcemanager_cancelrequest, strmif/IResourceManager::CancelRequest
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
 - IResourceManager::CancelRequest
 - strmif/IResourceManager::CancelRequest
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
 - IResourceManager.CancelRequest
---

# IResourceManager::CancelRequest


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>CancelRequest</code> method cancels the request for a resource.

## -parameters

### -param idResource [in]

Resource identifier of a pending request.

### -param pConsumer [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-iresourceconsumer">IResourceConsumer</a> interface that made the request.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation. <b>HRESULT</b> can be one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method isn't supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK or NOERROR</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

This method should be called when the <a href="/windows/desktop/api/strmif/nn-strmif-iresourceconsumer">IResourceConsumer</a> object that requested the resource has not received it and no longer requires it. If it has already received the resource, it should use the <a href="/windows/desktop/api/strmif/nf-strmif-iresourcemanager-notifyrelease">IResourceManager::NotifyRelease</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iresourcemanager">IResourceManager Interface</a>