---
UID: NF:strmif.IResourceManager.RegisterGroup
title: IResourceManager::RegisterGroup (strmif.h)
description: The RegisterGroup method registers a named resource group with the resource manager.
helpviewer_keywords: ["IResourceManager interface [DirectShow]","RegisterGroup method","IResourceManager.RegisterGroup","IResourceManager::RegisterGroup","IResourceManagerRegisterGroup","RegisterGroup","RegisterGroup method [DirectShow]","RegisterGroup method [DirectShow]","IResourceManager interface","dshow.iresourcemanager_registergroup","strmif/IResourceManager::RegisterGroup"]
old-location: dshow\iresourcemanager_registergroup.htm
tech.root: dshow
ms.assetid: f2d3deb2-8f22-42ac-846c-2f158f347ca7
ms.date: 4/26/2023
ms.keywords: IResourceManager interface [DirectShow],RegisterGroup method, IResourceManager.RegisterGroup, IResourceManager::RegisterGroup, IResourceManagerRegisterGroup, RegisterGroup, RegisterGroup method [DirectShow], RegisterGroup method [DirectShow],IResourceManager interface, dshow.iresourcemanager_registergroup, strmif/IResourceManager::RegisterGroup
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
 - IResourceManager::RegisterGroup
 - strmif/IResourceManager::RegisterGroup
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
 - IResourceManager.RegisterGroup
---

# IResourceManager::RegisterGroup


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>RegisterGroup</code> method registers a named resource group with the resource manager.

## -parameters

### -param pName [in]

Named resource group.

### -param cResource [in]

Number of resources in the group.

### -param palTokens [in]

Pointer to an array of resources in the group.

### -param plToken [out]

Pointer to the returned group resource identifier.

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iresourcemanager">IResourceManager Interface</a>