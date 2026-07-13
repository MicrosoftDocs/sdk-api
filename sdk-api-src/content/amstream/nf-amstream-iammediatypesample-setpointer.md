---
UID: NF:amstream.IAMMediaTypeSample.SetPointer
title: IAMMediaTypeSample::SetPointer (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetPointer method sets the pointer to the media sample's memory buffer.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","SetPointer method","IAMMediaTypeSample.SetPointer","IAMMediaTypeSample::SetPointer","IAMMediaTypeSampleSetPointer","SetPointer","SetPointer method [DirectShow]","SetPointer method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::SetPointer","dshow.iammediatypesample_setpointer"]
old-location: dshow\iammediatypesample_setpointer.htm
tech.root: dshow
ms.assetid: fc7a04c5-3542-41e0-8abc-bb7b40bff2c9
ms.date: 4/26/2023
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetPointer method, IAMMediaTypeSample.SetPointer, IAMMediaTypeSample::SetPointer, IAMMediaTypeSampleSetPointer, SetPointer, SetPointer method [DirectShow], SetPointer method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetPointer, dshow.iammediatypesample_setpointer
req.header: amstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaTypeSample::SetPointer
 - amstream/IAMMediaTypeSample::SetPointer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ext-ms-win-moderncore-win32k-base-ntuser-l1-1-0.dll
 - amstream.h
api_name:
 - IAMMediaTypeSample.SetPointer
---

# IAMMediaTypeSample::SetPointer


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetPointer</code> method sets the pointer to the media sample's memory buffer.

## -parameters

### -param pBuffer [in]

Pointer to a memory buffer allocated by the caller, or <b>NULL</b>.

### -param lSize [in]

Size of the buffer, in bytes.

## -returns

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
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
</table>

## -remarks

If the value of the <i>pBuffer</i> parameter is <b>NULL</b>, the method allocates a memory block, with a size in bytes equal to the value of the <i>lSize</i> parameter. There is no guarantee that the memory has been initialized.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>