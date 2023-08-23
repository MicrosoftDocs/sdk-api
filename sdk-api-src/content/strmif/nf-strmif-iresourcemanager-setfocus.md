---
UID: NF:strmif.IResourceManager.SetFocus
title: IResourceManager::SetFocus (strmif.h)
description: The SetFocus method notifies the resource manager that a specified object has been given the focus of the user.
helpviewer_keywords: ["IResourceManager interface [DirectShow]","SetFocus method","IResourceManager.SetFocus","IResourceManager::SetFocus","IResourceManagerSetFocus","SetFocus","SetFocus method [DirectShow]","SetFocus method [DirectShow]","IResourceManager interface","dshow.iresourcemanager_setfocus","strmif/IResourceManager::SetFocus"]
old-location: dshow\iresourcemanager_setfocus.htm
tech.root: dshow
ms.assetid: 3d0a87e1-6774-45cf-9ab5-18ec1d2fff0d
ms.date: 4/26/2023
ms.keywords: IResourceManager interface [DirectShow],SetFocus method, IResourceManager.SetFocus, IResourceManager::SetFocus, IResourceManagerSetFocus, SetFocus, SetFocus method [DirectShow], SetFocus method [DirectShow],IResourceManager interface, dshow.iresourcemanager_setfocus, strmif/IResourceManager::SetFocus
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
 - IResourceManager::SetFocus
 - strmif/IResourceManager::SetFocus
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
 - IResourceManager.SetFocus
---

# IResourceManager::SetFocus


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetFocus</code> method notifies the resource manager that a specified object has been given the focus of the user.

## -parameters

### -param pFocusObject [in]

Pointer to the object that has been given the user's focus.

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

In DirectShow, the object given the user's focus is typically a video renderer whose window has received the focus. The resource manager gives priority to requests for resources in the following order:

<ol>
<li>Requests made with the focus object specified in the <i>pFocusObject</i> parameter.</li>
<li>Requests whose focus object shares a common source filter.</li>
<li>Requests whose focus object shares a common filter graph.</li>
<li>Requests in the same process as the focus.</li>
</ol>
After a focus has been set, the resource manager must maintain a focus object until <a href="/windows/desktop/api/strmif/nf-strmif-iresourcemanager-releasefocus">ReleaseFocus</a> is called. That is, after calling this method, you must use <b>ReleaseFocus</b> before the <b>IUnknown</b> interface of the focus object becomes invalid, unless you can guarantee that <code>SetFocus</code> is called by a different object in the meantime. No reference count is held on the focus object.

The resource manager will hold this pointer until replaced or canceled, and will use it to resolve resource contention. It will use <b>QueryInterface</b> for the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface at least and, if found, will use methods on that interface. It calls methods on <b>IBaseFilter</b> to decide which audio renderer to use if there are two (it will choose the one with a source filter common to the focus object), and also to determine if the two objects are within the same filter graph.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iresourcemanager">IResourceManager Interface</a>