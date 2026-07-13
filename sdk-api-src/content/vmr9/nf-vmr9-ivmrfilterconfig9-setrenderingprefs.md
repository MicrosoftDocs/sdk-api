---
UID: NF:vmr9.IVMRFilterConfig9.SetRenderingPrefs
title: IVMRFilterConfig9::SetRenderingPrefs (vmr9.h)
description: The SetRenderingPrefs method sets various application preferences related to video rendering.
helpviewer_keywords: ["IVMRFilterConfig9 interface [DirectShow]","SetRenderingPrefs method","IVMRFilterConfig9.SetRenderingPrefs","IVMRFilterConfig9::SetRenderingPrefs","IVMRFilterConfig9SetRenderingPrefs","SetRenderingPrefs","SetRenderingPrefs method [DirectShow]","SetRenderingPrefs method [DirectShow]","IVMRFilterConfig9 interface","dshow.ivmrfilterconfig9_setrenderingprefs","vmr9/IVMRFilterConfig9::SetRenderingPrefs"]
old-location: dshow\ivmrfilterconfig9_setrenderingprefs.htm
tech.root: dshow
ms.assetid: ce274528-c759-4b43-80c7-0ba1e1275b7d
ms.date: 4/26/2023
ms.keywords: IVMRFilterConfig9 interface [DirectShow],SetRenderingPrefs method, IVMRFilterConfig9.SetRenderingPrefs, IVMRFilterConfig9::SetRenderingPrefs, IVMRFilterConfig9SetRenderingPrefs, SetRenderingPrefs, SetRenderingPrefs method [DirectShow], SetRenderingPrefs method [DirectShow],IVMRFilterConfig9 interface, dshow.ivmrfilterconfig9_setrenderingprefs, vmr9/IVMRFilterConfig9::SetRenderingPrefs
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
 - IVMRFilterConfig9::SetRenderingPrefs
 - vmr9/IVMRFilterConfig9::SetRenderingPrefs
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
 - IVMRFilterConfig9.SetRenderingPrefs
---

# IVMRFilterConfig9::SetRenderingPrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetRenderingPrefs</code> method sets various application preferences related to video rendering.

## -parameters

### -param dwRenderFlags [in]

Double word containing a bitwise OR of <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9renderprefs">VMR9RenderPrefs</a> values specifying the rendering preferences.

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
No allocator-presenter is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwRenderFlags</i> is invalid.

</td>
</tr>
</table>

## -remarks

This method calls through to the allocator-presenter's <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrimagepresenterconfig9-setrenderingprefs">IVMRImagePresenterConfig9::SetRenderingPrefs</a> method. (The default allocator-presenter exposes <b>IVMRImagePresenterConfig9</b>. Custom allocator-presenters can also expose this interface if desired.) If the VMR-9 has not yet created the default allocator-presenter, or if the application provided a custom allocator-presenter which does not support <b>IVMRImagePresenterConfig9</b>, this method returns VFW_E_WRONG_STATE. To create the default allocator-presenter, call <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode">IVMRFilterConfig9::SetRenderingMode</a> with the value VMR9Mode_Windowed or VMR9Mode_Windowed.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9">IVMRFilterConfig9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>