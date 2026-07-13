---
UID: NF:vmr9.IVMRFilterConfig9.SetImageCompositor
title: IVMRFilterConfig9::SetImageCompositor (vmr9.h)
description: The SetImageCompositor method installs an application-provided image compositor object.
helpviewer_keywords: ["IVMRFilterConfig9 interface [DirectShow]","SetImageCompositor method","IVMRFilterConfig9.SetImageCompositor","IVMRFilterConfig9::SetImageCompositor","IVMRFilterConfig9SetImageCompositor","SetImageCompositor","SetImageCompositor method [DirectShow]","SetImageCompositor method [DirectShow]","IVMRFilterConfig9 interface","dshow.ivmrfilterconfig9_setimagecompositor","vmr9/IVMRFilterConfig9::SetImageCompositor"]
old-location: dshow\ivmrfilterconfig9_setimagecompositor.htm
tech.root: dshow
ms.assetid: 8e4a66e8-d4ab-49e0-8773-c79b5965124b
ms.date: 4/26/2023
ms.keywords: IVMRFilterConfig9 interface [DirectShow],SetImageCompositor method, IVMRFilterConfig9.SetImageCompositor, IVMRFilterConfig9::SetImageCompositor, IVMRFilterConfig9SetImageCompositor, SetImageCompositor, SetImageCompositor method [DirectShow], SetImageCompositor method [DirectShow],IVMRFilterConfig9 interface, dshow.ivmrfilterconfig9_setimagecompositor, vmr9/IVMRFilterConfig9::SetImageCompositor
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
 - IVMRFilterConfig9::SetImageCompositor
 - vmr9/IVMRFilterConfig9::SetImageCompositor
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
 - IVMRFilterConfig9.SetImageCompositor
---

# IVMRFilterConfig9::SetImageCompositor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetImageCompositor</code> method installs an application-provided image compositor object.

## -parameters

### -param lpVMRImgCompositor [in]

Pointer to the image compositor object provided by the application.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Cannot change the compositor when the VMR filter's pins are connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer.

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in mixing mode.

</td>
</tr>
</table>

## -remarks

Use this method to replace the VMR's default compositor with a custom compositor provided by the application. The image compositor is a sub-component of the mixer. The mixer must be loaded, through a call to <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams">IVMRFilterConfig9::SetNumberOfStreams</a>,

before the compositor can be specified. The VMR manages all reference counting on the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagecompositor9">IVMRImageCompositor9</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9">IVMRFilterConfig9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>