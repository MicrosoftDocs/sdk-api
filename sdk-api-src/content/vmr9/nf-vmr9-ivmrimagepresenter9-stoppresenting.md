---
UID: NF:vmr9.IVMRImagePresenter9.StopPresenting
title: IVMRImagePresenter9::StopPresenting (vmr9.h)
description: The StopPresenting method is called just after the video stops playing. The allocator-presenter should perform any necessary cleanup in this method.
helpviewer_keywords: ["IVMRImagePresenter9 interface [DirectShow]","StopPresenting method","IVMRImagePresenter9.StopPresenting","IVMRImagePresenter9::StopPresenting","IVMRImagePresenter9StopPresenting","StopPresenting","StopPresenting method [DirectShow]","StopPresenting method [DirectShow]","IVMRImagePresenter9 interface","dshow.ivmrimagepresenter9_stoppresenting","vmr9/IVMRImagePresenter9::StopPresenting"]
old-location: dshow\ivmrimagepresenter9_stoppresenting.htm
tech.root: dshow
ms.assetid: 47f34048-3b07-464e-a1f2-f0b49fe76659
ms.date: 4/26/2023
ms.keywords: IVMRImagePresenter9 interface [DirectShow],StopPresenting method, IVMRImagePresenter9.StopPresenting, IVMRImagePresenter9::StopPresenting, IVMRImagePresenter9StopPresenting, StopPresenting, StopPresenting method [DirectShow], StopPresenting method [DirectShow],IVMRImagePresenter9 interface, dshow.ivmrimagepresenter9_stoppresenting, vmr9/IVMRImagePresenter9::StopPresenting
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
 - IVMRImagePresenter9::StopPresenting
 - vmr9/IVMRImagePresenter9::StopPresenting
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
 - IVMRImagePresenter9.StopPresenting
---

# IVMRImagePresenter9::StopPresenting


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>StopPresenting</code> method is called just after the video stops playing. The allocator-presenter should perform any necessary cleanup in this method.

## -parameters

### -param dwUserID [in]

An application-defined <b>DWORD_PTR</b> cookie that uniquely identifies this instance of the VMR for use in scenarios when one instance of the allocator-presenter is used with multiple VMR instances.

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

<code>StopPresenting</code> can be called only when the VMR is in a running state.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenter9">IVMRImagePresenter9 Interface</a>



<a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrimagepresenter9-startpresenting">StartPresenting</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>