---
UID: NF:vmr9.IVMRImageCompositor9.InitCompositionDevice
title: IVMRImageCompositor9::InitCompositionDevice (vmr9.h)
description: The InitCompositionDevice method informs the compositor that a new composition target has been created.
helpviewer_keywords: ["IVMRImageCompositor9 interface [DirectShow]","InitCompositionDevice method","IVMRImageCompositor9.InitCompositionDevice","IVMRImageCompositor9::InitCompositionDevice","IVMRImageCompositor9InitCompositionDevice","InitCompositionDevice","InitCompositionDevice method [DirectShow]","InitCompositionDevice method [DirectShow]","IVMRImageCompositor9 interface","dshow.ivmrimagecompositor9_initcompositiondevice","vmr9/IVMRImageCompositor9::InitCompositionDevice"]
old-location: dshow\ivmrimagecompositor9_initcompositiondevice.htm
tech.root: dshow
ms.assetid: 78381141-6b6d-4ed5-b8d3-aa1114fd9ac0
ms.date: 4/26/2023
ms.keywords: IVMRImageCompositor9 interface [DirectShow],InitCompositionDevice method, IVMRImageCompositor9.InitCompositionDevice, IVMRImageCompositor9::InitCompositionDevice, IVMRImageCompositor9InitCompositionDevice, InitCompositionDevice, InitCompositionDevice method [DirectShow], InitCompositionDevice method [DirectShow],IVMRImageCompositor9 interface, dshow.ivmrimagecompositor9_initcompositiondevice, vmr9/IVMRImageCompositor9::InitCompositionDevice
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
 - IVMRImageCompositor9::InitCompositionDevice
 - vmr9/IVMRImageCompositor9::InitCompositionDevice
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
 - IVMRImageCompositor9.InitCompositionDevice
---

# IVMRImageCompositor9::InitCompositionDevice


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>InitCompositionDevice</code> method informs the compositor that a new composition target has been created. The compositor should perform any necessary configuration work in this method. This could include attaching a Z or stencil buffer for the new render target.

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