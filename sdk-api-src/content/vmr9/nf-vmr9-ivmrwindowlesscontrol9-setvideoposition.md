---
UID: NF:vmr9.IVMRWindowlessControl9.SetVideoPosition
title: IVMRWindowlessControl9::SetVideoPosition (vmr9.h)
description: The SetVideoPosition method sets the source and destination rectangles for the video.
helpviewer_keywords: ["IVMRWindowlessControl9 interface [DirectShow]","SetVideoPosition method","IVMRWindowlessControl9.SetVideoPosition","IVMRWindowlessControl9::SetVideoPosition","IVMRWindowlessControl9SetVideoPosition","SetVideoPosition","SetVideoPosition method [DirectShow]","SetVideoPosition method [DirectShow]","IVMRWindowlessControl9 interface","dshow.ivmrwindowlesscontrol9_setvideoposition","vmr9/IVMRWindowlessControl9::SetVideoPosition"]
old-location: dshow\ivmrwindowlesscontrol9_setvideoposition.htm
tech.root: dshow
ms.assetid: 9b165b51-c60d-4039-b652-5a5347dec224
ms.date: 12/05/2018
ms.keywords: IVMRWindowlessControl9 interface [DirectShow],SetVideoPosition method, IVMRWindowlessControl9.SetVideoPosition, IVMRWindowlessControl9::SetVideoPosition, IVMRWindowlessControl9SetVideoPosition, SetVideoPosition, SetVideoPosition method [DirectShow], SetVideoPosition method [DirectShow],IVMRWindowlessControl9 interface, dshow.ivmrwindowlesscontrol9_setvideoposition, vmr9/IVMRWindowlessControl9::SetVideoPosition
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
 - IVMRWindowlessControl9::SetVideoPosition
 - vmr9/IVMRWindowlessControl9::SetVideoPosition
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
 - IVMRWindowlessControl9.SetVideoPosition
---

# IVMRWindowlessControl9::SetVideoPosition


## -description

The <code>SetVideoPosition</code> method sets the source and destination rectangles for the video.

## -parameters

### -param lpSRCRect [in]

Pointer to a <b>RECT</b> structure that specifies the source rectangle. If <b>NULL</b>, the source rectangle does not change. The default source rectangle is the entire video image.

### -param lpDSTRect [in]

Pointer to a <b>RECT</b> structure that specifies the destination rectangle. If <b>NULL</b>, the destination rectangle does not change. The default destination rectangle is {0, 0, 0, 0}.

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