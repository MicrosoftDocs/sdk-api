---
UID: NF:vmr9.IVMRFilterConfig9.GetRenderingPrefs
title: IVMRFilterConfig9::GetRenderingPrefs (vmr9.h)
description: The GetRenderingPrefs method retrieves the current set of rendering preferences being used by the VMR-9.
helpviewer_keywords: ["GetRenderingPrefs","GetRenderingPrefs method [DirectShow]","GetRenderingPrefs method [DirectShow]","IVMRFilterConfig9 interface","IVMRFilterConfig9 interface [DirectShow]","GetRenderingPrefs method","IVMRFilterConfig9.GetRenderingPrefs","IVMRFilterConfig9::GetRenderingPrefs","IVMRFilterConfig9GetRenderingPrefs","dshow.ivmrfilterconfig9_getrenderingprefs","vmr9/IVMRFilterConfig9::GetRenderingPrefs"]
old-location: dshow\ivmrfilterconfig9_getrenderingprefs.htm
tech.root: dshow
ms.assetid: b82a9dbe-aa86-4153-945b-fe8968faa5ca
ms.date: 4/26/2023
ms.keywords: GetRenderingPrefs, GetRenderingPrefs method [DirectShow], GetRenderingPrefs method [DirectShow],IVMRFilterConfig9 interface, IVMRFilterConfig9 interface [DirectShow],GetRenderingPrefs method, IVMRFilterConfig9.GetRenderingPrefs, IVMRFilterConfig9::GetRenderingPrefs, IVMRFilterConfig9GetRenderingPrefs, dshow.ivmrfilterconfig9_getrenderingprefs, vmr9/IVMRFilterConfig9::GetRenderingPrefs
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
 - IVMRFilterConfig9::GetRenderingPrefs
 - vmr9/IVMRFilterConfig9::GetRenderingPrefs
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
 - IVMRFilterConfig9.GetRenderingPrefs
---

# IVMRFilterConfig9::GetRenderingPrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetRenderingPrefs</b> method retrieves the current set of rendering preferences being used by the VMR-9.

## -parameters

### -param pdwRenderFlags [out]

Receives a <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9renderprefs">VMR9RenderPrefs</a> value indicating the current rendering preferences.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR has not created an allocator-presenter, or the allocator-presenter does not implement the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenterconfig9">IVMRImagePresenterConfig9</a> interface.

</td>
</tr>
</table>

## -remarks

If  the allocator-presenter implements the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenterconfig9">IVMRImagePresenterConfig9</a> interface, this method calls the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrimagepresenterconfig9-getrenderingprefs">IVMRImagePresenterConfig9::GetRenderingPrefs</a> method on the allocator-presenter. 

The default allocator-presenter implements <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenterconfig9">IVMRImagePresenterConfig9</a>. Custom allocator-presenters can also implements this interface if desired.

If the VMR-9 has not yet created the allocator-presenter, or if a custom allocator-presenter does not support <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenterconfig9">IVMRImagePresenterConfig9</a>, this method returns <b>VFW_E_WRONG_STATE</b>. To create the default allocator-presenter, call <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode">IVMRFilterConfig9::SetRenderingMode</a> with the value <b>VMR9Mode_Windowed</b> or <b>VMR9Mode_Windowless</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9">IVMRFilterConfig9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>