---
UID: NF:vmr9.IVMRWindowlessControl9.GetVideoPosition
title: IVMRWindowlessControl9::GetVideoPosition (vmr9.h)
description: The GetVideoPosition method retrieves the current source and destination rectangles used to display the video.helpviewer_keywords: ["GetVideoPosition","GetVideoPosition method [DirectShow]","GetVideoPosition method [DirectShow]","IVMRWindowlessControl9 interface","IVMRWindowlessControl9 interface [DirectShow]","GetVideoPosition method","IVMRWindowlessControl9.GetVideoPosition","IVMRWindowlessControl9::GetVideoPosition","IVMRWindowlessControl9GetVideoPosition","dshow.ivmrwindowlesscontrol9_getvideoposition","vmr9/IVMRWindowlessControl9::GetVideoPosition"]
old-location: dshow\ivmrwindowlesscontrol9_getvideoposition.htm
tech.root: DirectShow
ms.assetid: 0963ec09-8637-441c-b10e-fecc11788e39
ms.date: 12/05/2018
ms.keywords: GetVideoPosition, GetVideoPosition method [DirectShow], GetVideoPosition method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetVideoPosition method, IVMRWindowlessControl9.GetVideoPosition, IVMRWindowlessControl9::GetVideoPosition, IVMRWindowlessControl9GetVideoPosition, dshow.ivmrwindowlesscontrol9_getvideoposition, vmr9/IVMRWindowlessControl9::GetVideoPosition
f1_keywords:
- vmr9/IVMRWindowlessControl9.GetVideoPosition
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IVMRWindowlessControl9.GetVideoPosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl9::GetVideoPosition


## -description



The <code>GetVideoPosition</code> method retrieves the current source and destination rectangles used to display the video.




## -parameters




### -param lpSRCRect [out]

Pointer that receives the current source rectangle.


### -param lpDSTRect [out]

Pointer that receives the current destination rectangle.


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




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrwindowlesscontrol9">IVMRWindowlessControl9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition">SetVideoPosition</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

