---
UID: NF:vmr9.IVMRAspectRatioControl9.GetAspectRatioMode
title: IVMRAspectRatioControl9::GetAspectRatioMode (vmr9.h)
description: The GetAspectRatioMode method queries whether the VMR preserves the aspect ratio of the source video.
helpviewer_keywords: ["GetAspectRatioMode","GetAspectRatioMode method [DirectShow]","GetAspectRatioMode method [DirectShow]","IVMRAspectRatioControl9 interface","IVMRAspectRatioControl9 interface [DirectShow]","GetAspectRatioMode method","IVMRAspectRatioControl9.GetAspectRatioMode","IVMRAspectRatioControl9::GetAspectRatioMode","IVMRAspectRatioControl9GetAspectRatioMode","dshow.ivmraspectratiocontrol9_getaspectratiomode","vmr9/IVMRAspectRatioControl9::GetAspectRatioMode"]
old-location: dshow\ivmraspectratiocontrol9_getaspectratiomode.htm
tech.root: dshow
ms.assetid: e53e9015-5186-4807-a5ee-af8598a89a2b
ms.date: 4/26/2023
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [DirectShow], GetAspectRatioMode method [DirectShow],IVMRAspectRatioControl9 interface, IVMRAspectRatioControl9 interface [DirectShow],GetAspectRatioMode method, IVMRAspectRatioControl9.GetAspectRatioMode, IVMRAspectRatioControl9::GetAspectRatioMode, IVMRAspectRatioControl9GetAspectRatioMode, dshow.ivmraspectratiocontrol9_getaspectratiomode, vmr9/IVMRAspectRatioControl9::GetAspectRatioMode
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
 - IVMRAspectRatioControl9::GetAspectRatioMode
 - vmr9/IVMRAspectRatioControl9::GetAspectRatioMode
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
 - IVMRAspectRatioControl9.GetAspectRatioMode
---

# IVMRAspectRatioControl9::GetAspectRatioMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAspectRatioMode</code> method queries whether the VMR preserves the aspect ratio of the source video.

## -parameters

### -param lpdwARMode [out]

Pointer to a variable that receives a member of the <a href="/windows/desktop/api/strmif/ne-strmif-vmr_aspect_ratio_mode">VMR_ASPECT_RATIO_MODE</a> enumeration.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmraspectratiocontrol9">IVMRAspectRatioControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>