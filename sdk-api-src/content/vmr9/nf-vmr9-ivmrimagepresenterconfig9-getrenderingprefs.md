---
UID: NF:vmr9.IVMRImagePresenterConfig9.GetRenderingPrefs
title: IVMRImagePresenterConfig9::GetRenderingPrefs (vmr9.h)
description: The GetRenderingPrefs method gets the current rendering preferences from the VMR-9 filter's allocator-presenter.
helpviewer_keywords: ["GetRenderingPrefs","GetRenderingPrefs method [DirectShow]","GetRenderingPrefs method [DirectShow]","IVMRImagePresenterConfig9 interface","IVMRImagePresenterConfig9 interface [DirectShow]","GetRenderingPrefs method","IVMRImagePresenterConfig9.GetRenderingPrefs","IVMRImagePresenterConfig9::GetRenderingPrefs","IVMRImagePresenterConfig9GetRenderingPrefs","dshow.ivmrimagepresenterconfig9_getrenderingprefs","vmr9/IVMRImagePresenterConfig9::GetRenderingPrefs"]
old-location: dshow\ivmrimagepresenterconfig9_getrenderingprefs.htm
tech.root: dshow
ms.assetid: dfa9c81d-cfc8-401b-b4d1-50f21b528135
ms.date: 4/26/2023
ms.keywords: GetRenderingPrefs, GetRenderingPrefs method [DirectShow], GetRenderingPrefs method [DirectShow],IVMRImagePresenterConfig9 interface, IVMRImagePresenterConfig9 interface [DirectShow],GetRenderingPrefs method, IVMRImagePresenterConfig9.GetRenderingPrefs, IVMRImagePresenterConfig9::GetRenderingPrefs, IVMRImagePresenterConfig9GetRenderingPrefs, dshow.ivmrimagepresenterconfig9_getrenderingprefs, vmr9/IVMRImagePresenterConfig9::GetRenderingPrefs
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
 - IVMRImagePresenterConfig9::GetRenderingPrefs
 - vmr9/IVMRImagePresenterConfig9::GetRenderingPrefs
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
 - IVMRImagePresenterConfig9.GetRenderingPrefs
---

# IVMRImagePresenterConfig9::GetRenderingPrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetRenderingPrefs</code> method gets the current rendering preferences from the VMR-9 filter's allocator-presenter.



The VMR-9 filter's <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-getrenderingprefs">IVMRFilterConfig9::GetRenderingPrefs</a> method calls through to this method.

## -parameters

### -param dwRenderFlags [out]

Receives a bitwise OR of flag from the <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9renderprefs">VMR9RenderPrefs</a> enumeration, indicating the current rendering settings on the allocator-presenter.

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

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenterconfig9">IVMRImagePresenterConfig9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>