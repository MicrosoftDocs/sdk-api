---
UID: NF:vmr9.IVMRWindowlessControl9.GetAspectRatioMode
title: IVMRWindowlessControl9::GetAspectRatioMode (vmr9.h)
description: The GetAspectRatioMode method retrieves the current aspect ratio display mode.
helpviewer_keywords: ["GetAspectRatioMode","GetAspectRatioMode method [DirectShow]","GetAspectRatioMode method [DirectShow]","IVMRWindowlessControl9 interface","IVMRWindowlessControl9 interface [DirectShow]","GetAspectRatioMode method","IVMRWindowlessControl9.GetAspectRatioMode","IVMRWindowlessControl9::GetAspectRatioMode","IVMRWindowlessControl9GetAspectRatioMode","dshow.ivmrwindowlesscontrol9_getaspectratiomode","vmr9/IVMRWindowlessControl9::GetAspectRatioMode"]
old-location: dshow\ivmrwindowlesscontrol9_getaspectratiomode.htm
tech.root: dshow
ms.assetid: c18ab567-5e0d-400a-8dc1-e9ad83650b7c
ms.date: 4/26/2023
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [DirectShow], GetAspectRatioMode method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetAspectRatioMode method, IVMRWindowlessControl9.GetAspectRatioMode, IVMRWindowlessControl9::GetAspectRatioMode, IVMRWindowlessControl9GetAspectRatioMode, dshow.ivmrwindowlesscontrol9_getaspectratiomode, vmr9/IVMRWindowlessControl9::GetAspectRatioMode
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
 - IVMRWindowlessControl9::GetAspectRatioMode
 - vmr9/IVMRWindowlessControl9::GetAspectRatioMode
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
 - IVMRWindowlessControl9.GetAspectRatioMode
---

# IVMRWindowlessControl9::GetAspectRatioMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAspectRatioMode</code> method retrieves the current aspect ratio display mode.

## -parameters

### -param lpAspectRatioMode [out]

Pointer to a DWORD that receives a <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9aspectratiomode">VMR9AspectRatioMode</a> value that indicates the current aspect ratio mode.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>lpAspectRatioMode</i> is invalid

</td>
</tr>
</table>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/ms787155(v=vs.85)">IVMRWindowlessControl9 Interface</a>



<a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode">SetAspectRatioMode</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>