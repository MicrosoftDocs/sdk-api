---
UID: NF:vmr9.IVMRWindowlessControl9.GetMinIdealVideoSize
title: IVMRWindowlessControl9::GetMinIdealVideoSize (vmr9.h)
description: The GetMinIdealVideoSize method retrieves the minimum video size that the VMR can display without incurring significant performance or image quality degradation.
helpviewer_keywords: ["GetMinIdealVideoSize","GetMinIdealVideoSize method [DirectShow]","GetMinIdealVideoSize method [DirectShow]","IVMRWindowlessControl9 interface","IVMRWindowlessControl9 interface [DirectShow]","GetMinIdealVideoSize method","IVMRWindowlessControl9.GetMinIdealVideoSize","IVMRWindowlessControl9::GetMinIdealVideoSize","IVMRWindowlessControl9GetMinIdealVideoSize","dshow.ivmrwindowlesscontrol9_getminidealvideosize","vmr9/IVMRWindowlessControl9::GetMinIdealVideoSize"]
old-location: dshow\ivmrwindowlesscontrol9_getminidealvideosize.htm
tech.root: dshow
ms.assetid: 9e100f04-28fc-4449-9fe4-0f0074e6439c
ms.date: 12/05/2018
ms.keywords: GetMinIdealVideoSize, GetMinIdealVideoSize method [DirectShow], GetMinIdealVideoSize method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetMinIdealVideoSize method, IVMRWindowlessControl9.GetMinIdealVideoSize, IVMRWindowlessControl9::GetMinIdealVideoSize, IVMRWindowlessControl9GetMinIdealVideoSize, dshow.ivmrwindowlesscontrol9_getminidealvideosize, vmr9/IVMRWindowlessControl9::GetMinIdealVideoSize
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
 - IVMRWindowlessControl9::GetMinIdealVideoSize
 - vmr9/IVMRWindowlessControl9::GetMinIdealVideoSize
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
 - IVMRWindowlessControl9.GetMinIdealVideoSize
---

# IVMRWindowlessControl9::GetMinIdealVideoSize


## -description

The <code>GetMinIdealVideoSize</code> method retrieves the minimum video size that the VMR can display without incurring significant performance or image quality degradation.

## -parameters

### -param lpWidth [out]

Pointer that receives the minimum ideal width.

### -param lpHeight [out]

Pointer that receives the minimum ideal height.

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

<a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getmaxidealvideosize">GetMaxIdealVideoSize</a>



<a href="/previous-versions/ms787155(v=vs.85)">IVMRWindowlessControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>