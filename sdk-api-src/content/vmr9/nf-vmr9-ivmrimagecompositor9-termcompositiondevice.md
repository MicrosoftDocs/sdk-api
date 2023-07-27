---
UID: NF:vmr9.IVMRImageCompositor9.TermCompositionDevice
title: IVMRImageCompositor9::TermCompositionDevice (vmr9.h)
description: The TermCompositionDevice method informs the compositor that the current composition target is being replaced. Compositors should perform any necessary cleanup of the composition target in this method.
helpviewer_keywords: ["IVMRImageCompositor9 interface [DirectShow]","TermCompositionDevice method","IVMRImageCompositor9.TermCompositionDevice","IVMRImageCompositor9::TermCompositionDevice","IVMRImageCompositor9TermCompositionDevice","TermCompositionDevice","TermCompositionDevice method [DirectShow]","TermCompositionDevice method [DirectShow]","IVMRImageCompositor9 interface","dshow.ivmrimagecompositor9_termcompositiondevice","vmr9/IVMRImageCompositor9::TermCompositionDevice"]
old-location: dshow\ivmrimagecompositor9_termcompositiondevice.htm
tech.root: dshow
ms.assetid: e218222b-fed3-4f4b-8d97-785774800d89
ms.date: 4/26/2023
ms.keywords: IVMRImageCompositor9 interface [DirectShow],TermCompositionDevice method, IVMRImageCompositor9.TermCompositionDevice, IVMRImageCompositor9::TermCompositionDevice, IVMRImageCompositor9TermCompositionDevice, TermCompositionDevice, TermCompositionDevice method [DirectShow], TermCompositionDevice method [DirectShow],IVMRImageCompositor9 interface, dshow.ivmrimagecompositor9_termcompositiondevice, vmr9/IVMRImageCompositor9::TermCompositionDevice
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
 - IVMRImageCompositor9::TermCompositionDevice
 - vmr9/IVMRImageCompositor9::TermCompositionDevice
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
 - IVMRImageCompositor9.TermCompositionDevice
---

# IVMRImageCompositor9::TermCompositionDevice


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>TermCompositionDevice</code> method informs the compositor that the current composition target is being replaced. Compositors should perform any necessary cleanup of the composition target in this method.

## -parameters

### -param pD3DDevice [in]

Pointer to the <b>IUnknown</b> interface of the Direct3D device object.

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