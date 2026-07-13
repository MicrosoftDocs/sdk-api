---
UID: NF:strmif.IMemAllocator.GetProperties
title: IMemAllocator::GetProperties (strmif.h)
description: The GetProperties method retrieves the number of buffers that the allocator will create, and the buffer properties.
helpviewer_keywords: ["GetProperties","GetProperties method [DirectShow]","GetProperties method [DirectShow]","IMemAllocator interface","IMemAllocator interface [DirectShow]","GetProperties method","IMemAllocator.GetProperties","IMemAllocator::GetProperties","IMemAllocatorGetProperties","dshow.imemallocator_getproperties","strmif/IMemAllocator::GetProperties"]
old-location: dshow\imemallocator_getproperties.htm
tech.root: dshow
ms.assetid: d7b7153c-24c4-4508-925b-b5cfbc26badc
ms.date: 4/26/2023
ms.keywords: GetProperties, GetProperties method [DirectShow], GetProperties method [DirectShow],IMemAllocator interface, IMemAllocator interface [DirectShow],GetProperties method, IMemAllocator.GetProperties, IMemAllocator::GetProperties, IMemAllocatorGetProperties, dshow.imemallocator_getproperties, strmif/IMemAllocator::GetProperties
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
 - IMemAllocator::GetProperties
 - strmif/IMemAllocator::GetProperties
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
 - IMemAllocator.GetProperties
---

# IMemAllocator::GetProperties


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetProperties</code> method retrieves the number of buffers that the allocator will create, and the buffer properties.

## -parameters

### -param pProps [out]

Pointer to an [ALLOCATOR_PROPERTIES](/windows/desktop/api/strmif/ns-strmif-allocator_properties) structure that receives the allocator properties.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

Calls to this method might not succeed until the <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-commit">IMemAllocator::Commit</a> method is called.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator Interface</a>