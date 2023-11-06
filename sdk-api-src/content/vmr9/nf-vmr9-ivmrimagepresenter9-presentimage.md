---
UID: NF:vmr9.IVMRImagePresenter9.PresentImage
title: IVMRImagePresenter9::PresentImage (vmr9.h)
description: The PresentImage method is called at precisely the moment this video frame should be presented.
helpviewer_keywords: ["IVMRImagePresenter9 interface [DirectShow]","PresentImage method","IVMRImagePresenter9.PresentImage","IVMRImagePresenter9::PresentImage","IVMRImagePresenter9PresentImage","PresentImage","PresentImage method [DirectShow]","PresentImage method [DirectShow]","IVMRImagePresenter9 interface","dshow.ivmrimagepresenter9_presentimage","vmr9/IVMRImagePresenter9::PresentImage"]
old-location: dshow\ivmrimagepresenter9_presentimage.htm
tech.root: dshow
ms.assetid: 1c642958-88df-48b2-8eb1-0d032af71f71
ms.date: 4/26/2023
ms.keywords: IVMRImagePresenter9 interface [DirectShow],PresentImage method, IVMRImagePresenter9.PresentImage, IVMRImagePresenter9::PresentImage, IVMRImagePresenter9PresentImage, PresentImage, PresentImage method [DirectShow], PresentImage method [DirectShow],IVMRImagePresenter9 interface, dshow.ivmrimagepresenter9_presentimage, vmr9/IVMRImagePresenter9::PresentImage
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
 - IVMRImagePresenter9::PresentImage
 - vmr9/IVMRImagePresenter9::PresentImage
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
 - IVMRImagePresenter9.PresentImage
---

# IVMRImagePresenter9::PresentImage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>PresentImage</code> method is called at precisely the moment this video frame should be presented.

## -parameters

### -param dwUserID [in]

An application-defined DWORD_PTR that uniquely identifies this instance of the VMR in scenarios when multiple instances of the VMR are being used with a single instance of an allocator-presenter. See Remarks.

### -param lpPresInfo [in]

Specifies a <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9presentationinfo">VMR9PresentationInfo</a> structure that contains information about the video frame.

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

<code>PresentImage</code> can be called when the filter is in either a running or a paused state. <b>StartPresenting</b> and <b>StopPresenting</b> can be called only in a running state. Therefore, if the graph is paused before it is run, <code>PresentImage</code> will be called before <b>StartPresenting</b>.

Applications can create custom blending effects by using a single instance of an allocator-presenter with multiple instances of the VMR either in a single filter graph or in multiple filter graphs. Using the allocator presenter in this way enables applications to blend streams from different filter graphs, or blend different streams within the same filter graph. If you are using a single instance of the VMR, set this value to zero.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenter9">IVMRImagePresenter9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>