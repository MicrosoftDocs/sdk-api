---
UID: NF:vmr9.IVMRImageCompositor9.SetStreamMediaType
title: IVMRImageCompositor9::SetStreamMediaType (vmr9.h)
description: The SetStreamMediaType method sets the media type for the input stream.
helpviewer_keywords: ["IVMRImageCompositor9 interface [DirectShow]","SetStreamMediaType method","IVMRImageCompositor9.SetStreamMediaType","IVMRImageCompositor9::SetStreamMediaType","IVMRImageCompositor9SetStreamMediaType","SetStreamMediaType","SetStreamMediaType method [DirectShow]","SetStreamMediaType method [DirectShow]","IVMRImageCompositor9 interface","dshow.ivmrimagecompositor9_setstreammediatype","vmr9/IVMRImageCompositor9::SetStreamMediaType"]
old-location: dshow\ivmrimagecompositor9_setstreammediatype.htm
tech.root: dshow
ms.assetid: 4d994a83-a5be-427c-bf19-0090577d6ee5
ms.date: 4/26/2023
ms.keywords: IVMRImageCompositor9 interface [DirectShow],SetStreamMediaType method, IVMRImageCompositor9.SetStreamMediaType, IVMRImageCompositor9::SetStreamMediaType, IVMRImageCompositor9SetStreamMediaType, SetStreamMediaType, SetStreamMediaType method [DirectShow], SetStreamMediaType method [DirectShow],IVMRImageCompositor9 interface, dshow.ivmrimagecompositor9_setstreammediatype, vmr9/IVMRImageCompositor9::SetStreamMediaType
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVMRImageCompositor9::SetStreamMediaType
 - vmr9/IVMRImageCompositor9::SetStreamMediaType
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
 - IVMRImageCompositor9.SetStreamMediaType
---

# IVMRImageCompositor9::SetStreamMediaType


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetStreamMediaType</code> method sets the media type for the input stream.

## -parameters

### -param dwStrmID [in]

Specifies the input stream; must be from 1 through 16.

### -param pmt [in]

Pointer to the AM_MEDIA_TYPE struct that specifies the media type.

### -param fTexture [in]

If <b>TRUE</b>, specifies that the target surface is a Direct3D texture surface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagecompositor9">IVMRImageCompositor9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>