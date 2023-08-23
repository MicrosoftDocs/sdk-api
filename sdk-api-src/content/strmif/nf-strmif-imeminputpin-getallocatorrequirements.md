---
UID: NF:strmif.IMemInputPin.GetAllocatorRequirements
title: IMemInputPin::GetAllocatorRequirements (strmif.h)
description: The GetAllocatorRequirements method retrieves the allocator properties requested by the input pin.
helpviewer_keywords: ["GetAllocatorRequirements","GetAllocatorRequirements method [DirectShow]","GetAllocatorRequirements method [DirectShow]","IMemInputPin interface","IMemInputPin interface [DirectShow]","GetAllocatorRequirements method","IMemInputPin.GetAllocatorRequirements","IMemInputPin::GetAllocatorRequirements","IMemInputPinGetAllocatorRequirements","dshow.imeminputpin_getallocatorrequirements","strmif/IMemInputPin::GetAllocatorRequirements"]
old-location: dshow\imeminputpin_getallocatorrequirements.htm
tech.root: dshow
ms.assetid: 61e6ea4f-70cd-43d8-bbb7-76e041ee0eeb
ms.date: 4/26/2023
ms.keywords: GetAllocatorRequirements, GetAllocatorRequirements method [DirectShow], GetAllocatorRequirements method [DirectShow],IMemInputPin interface, IMemInputPin interface [DirectShow],GetAllocatorRequirements method, IMemInputPin.GetAllocatorRequirements, IMemInputPin::GetAllocatorRequirements, IMemInputPinGetAllocatorRequirements, dshow.imeminputpin_getallocatorrequirements, strmif/IMemInputPin::GetAllocatorRequirements
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
 - IMemInputPin::GetAllocatorRequirements
 - strmif/IMemInputPin::GetAllocatorRequirements
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
 - IMemInputPin.GetAllocatorRequirements
---

# IMemInputPin::GetAllocatorRequirements


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAllocatorRequirements</code> method retrieves the allocator properties requested by the input pin.

## -parameters

### -param pProps [out]

Pointer to an [ALLOCATOR_PROPERTIES](/windows/desktop/api/strmif/ns-strmif-allocator_properties), structure which is filled in with the requirements.

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
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
</table>

## -remarks

When an output pin initializes a memory allocator, it can call this method to determine whether the input pin has any buffer requirements. The input pin is not required to implement this method. If the filter has specific alignment or prefix requirements, it should implement this method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin Interface</a>
