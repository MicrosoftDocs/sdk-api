---
UID: NF:strmif.IResourceManager.NotifyRelease
title: IResourceManager::NotifyRelease (strmif.h)
description: The NotifyRelease method notifies the resource manager that IResourceConsumer has released a resource.
helpviewer_keywords: ["IResourceManager interface [DirectShow]","NotifyRelease method","IResourceManager.NotifyRelease","IResourceManager::NotifyRelease","IResourceManagerNotifyRelease","NotifyRelease","NotifyRelease method [DirectShow]","NotifyRelease method [DirectShow]","IResourceManager interface","dshow.iresourcemanager_notifyrelease","strmif/IResourceManager::NotifyRelease"]
old-location: dshow\iresourcemanager_notifyrelease.htm
tech.root: dshow
ms.assetid: a3779a8d-fe78-4f9b-af6c-7a25e0f07a86
ms.date: 4/26/2023
ms.keywords: IResourceManager interface [DirectShow],NotifyRelease method, IResourceManager.NotifyRelease, IResourceManager::NotifyRelease, IResourceManagerNotifyRelease, NotifyRelease, NotifyRelease method [DirectShow], NotifyRelease method [DirectShow],IResourceManager interface, dshow.iresourcemanager_notifyrelease, strmif/IResourceManager::NotifyRelease
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
 - IResourceManager::NotifyRelease
 - strmif/IResourceManager::NotifyRelease
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
 - IResourceManager.NotifyRelease
---

# IResourceManager::NotifyRelease


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>NotifyRelease</code> method notifies the resource manager that <a href="/windows/desktop/api/strmif/nn-strmif-iresourceconsumer">IResourceConsumer</a> has released a resource.

## -parameters

### -param idResource [in]

Resource token.

### -param pConsumer [in]

Pointer to the object releasing the resource.

### -param bStillWant [in]

Flag that specifies whether the resource is still required. Set to <b>TRUE</b> to indicate that you still want the resource when it is next available, or <b>FALSE</b> if you no longer want the resource.

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

Use this method in response to an <a href="/windows/desktop/api/strmif/nf-strmif-iresourceconsumer-releaseresource">IResourceConsumer::ReleaseResource</a> method, or when you have finished using the resource.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iresourcemanager">IResourceManager Interface</a>