---
UID: NF:strmif.IMemAllocator.SetProperties
title: IMemAllocator::SetProperties (strmif.h)
description: The SetProperties method specifies the number of buffers to allocate and the size of each buffer.
helpviewer_keywords: ["IMemAllocator interface [DirectShow]","SetProperties method","IMemAllocator.SetProperties","IMemAllocator::SetProperties","IMemAllocatorSetProperties","SetProperties","SetProperties method [DirectShow]","SetProperties method [DirectShow]","IMemAllocator interface","dshow.imemallocator_setproperties","strmif/IMemAllocator::SetProperties"]
old-location: dshow\imemallocator_setproperties.htm
tech.root: dshow
ms.assetid: c68f2e2f-c70f-447d-804b-dfdfe8ae8a52
ms.date: 4/26/2023
ms.keywords: IMemAllocator interface [DirectShow],SetProperties method, IMemAllocator.SetProperties, IMemAllocator::SetProperties, IMemAllocatorSetProperties, SetProperties, SetProperties method [DirectShow], SetProperties method [DirectShow],IMemAllocator interface, dshow.imemallocator_setproperties, strmif/IMemAllocator::SetProperties
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
 - IMemAllocator::SetProperties
 - strmif/IMemAllocator::SetProperties
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
 - IMemAllocator.SetProperties
---

# IMemAllocator::SetProperties


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetProperties</code> method specifies the number of buffers to allocate and the size of each buffer.

## -parameters

### -param pRequest

Pointer to an [ALLOCATOR_PROPERTIES](/windows/desktop/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.

### -param pActual

Pointer to an <b>ALLOCATOR_PROPERTIES</b> structure that receives the actual buffer properties.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
Success.

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
<dt><b>VFW_E_ALREADY_COMMITTED</b></dt>
</dl>
</td>
<td width="60%">
Cannot change allocated memory while the filter is active.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_BADALIGN</b></dt>
</dl>
</td>
<td width="60%">
An invalid alignment was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_BUFFERS_OUTSTANDING</b></dt>
</dl>
</td>
<td width="60%">
One or more buffers are still active.

</td>
</tr>
</table>

## -remarks

This method specifies the buffer requirements, but does not allocate any buffers. Call the <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-commit">IMemAllocator::Commit</a> method to allocate buffers.

The caller allocates two ALLOCATOR_PROPERTIES structures. The <i>pRequest</i> parameter contains the caller's buffer requirements, including the number of buffers and the size of each buffer. When the method returns, the <i>pActual</i> parameter contains the actual buffer properties, as set by the allocator.

When this method is called, the allocator must not be committed or have outstanding buffers.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator Interface</a>