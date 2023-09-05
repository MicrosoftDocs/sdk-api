---
UID: NF:strmif.IResourceManager.NotifyAcquire
title: IResourceManager::NotifyAcquire (strmif.h)
description: The NotifyAcquire method notifies the resource manager that an attempt to acquire a resource has completed.
helpviewer_keywords: ["IResourceManager interface [DirectShow]","NotifyAcquire method","IResourceManager.NotifyAcquire","IResourceManager::NotifyAcquire","IResourceManagerNotifyAcquire","NotifyAcquire","NotifyAcquire method [DirectShow]","NotifyAcquire method [DirectShow]","IResourceManager interface","dshow.iresourcemanager_notifyacquire","strmif/IResourceManager::NotifyAcquire"]
old-location: dshow\iresourcemanager_notifyacquire.htm
tech.root: dshow
ms.assetid: a5c52f5b-1c21-4f4c-b698-15b6ec7f7fed
ms.date: 4/26/2023
ms.keywords: IResourceManager interface [DirectShow],NotifyAcquire method, IResourceManager.NotifyAcquire, IResourceManager::NotifyAcquire, IResourceManagerNotifyAcquire, NotifyAcquire, NotifyAcquire method [DirectShow], NotifyAcquire method [DirectShow],IResourceManager interface, dshow.iresourcemanager_notifyacquire, strmif/IResourceManager::NotifyAcquire
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
 - IResourceManager::NotifyAcquire
 - strmif/IResourceManager::NotifyAcquire
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
 - IResourceManager.NotifyAcquire
---

# IResourceManager::NotifyAcquire


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>NotifyAcquire</code> method notifies the resource manager that an attempt to acquire a resource has completed.

## -parameters

### -param idResource [in]

Token for the registered resource.

### -param pConsumer [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-iresourceconsumer">IResourceConsumer</a> interface of the object requesting the resource.

### -param hr [in]

Value indicating the success of the acquisition; S_OK if the resource was acquired, or an error value if not.

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

Use this method after an <a href="/windows/desktop/api/strmif/nf-strmif-iresourceconsumer-acquireresource">IResourceConsumer::AcquireResource</a> method returns an S_FALSE value, indicating that the acquisition will be asynchronous (that is, handled by a callback mechanism). If the <i>hr</i> parameter is S_OK, the resource manager will assume that the resource is now held by the caller. If the <i>hr</i> parameter is anything other than S_OK, the resource manager will assume that the attempt to acquire the resource failed and will reassign the resource elsewhere.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iresourcemanager">IResourceManager Interface</a>