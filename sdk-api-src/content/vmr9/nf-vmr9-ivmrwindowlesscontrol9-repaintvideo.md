---
UID: NF:vmr9.IVMRWindowlessControl9.RepaintVideo
title: IVMRWindowlessControl9::RepaintVideo (vmr9.h)
description: The RepaintVideo method repaints the current video frame.
helpviewer_keywords: ["IVMRWindowlessControl9 interface [DirectShow]","RepaintVideo method","IVMRWindowlessControl9.RepaintVideo","IVMRWindowlessControl9::RepaintVideo","IVMRWindowlessControl9RepaintVideo","RepaintVideo","RepaintVideo method [DirectShow]","RepaintVideo method [DirectShow]","IVMRWindowlessControl9 interface","dshow.ivmrwindowlesscontrol9_repaintvideo","vmr9/IVMRWindowlessControl9::RepaintVideo"]
old-location: dshow\ivmrwindowlesscontrol9_repaintvideo.htm
tech.root: dshow
ms.assetid: 7a25301c-00e4-4f54-a34d-416a52daeaa7
ms.date: 12/05/2018
ms.keywords: IVMRWindowlessControl9 interface [DirectShow],RepaintVideo method, IVMRWindowlessControl9.RepaintVideo, IVMRWindowlessControl9::RepaintVideo, IVMRWindowlessControl9RepaintVideo, RepaintVideo, RepaintVideo method [DirectShow], RepaintVideo method [DirectShow],IVMRWindowlessControl9 interface, dshow.ivmrwindowlesscontrol9_repaintvideo, vmr9/IVMRWindowlessControl9::RepaintVideo
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
 - IVMRWindowlessControl9::RepaintVideo
 - vmr9/IVMRWindowlessControl9::RepaintVideo
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
 - IVMRWindowlessControl9.RepaintVideo
---

# IVMRWindowlessControl9::RepaintVideo


## -description

The <code>RepaintVideo</code> method repaints the current video frame.

## -parameters

### -param hwnd [in]

Specifies the handle of the window in which the repainting should occur.

### -param hdc [in]

Specifies the handle to the device context for the window.

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
The VMR is not in windowless mode.

</td>
</tr>
</table>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/ms787155(v=vs.85)">IVMRWindowlessControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>