---
UID: NF:vmr9.IVMRWindowlessControl9.GetMaxIdealVideoSize
title: IVMRWindowlessControl9::GetMaxIdealVideoSize (vmr9.h)
description: The GetMaxIdealVideoSize method retrieves the maximum video size that the VMR can display without incurring significant performance or image quality degradation.
helpviewer_keywords: ["GetMaxIdealVideoSize","GetMaxIdealVideoSize method [DirectShow]","GetMaxIdealVideoSize method [DirectShow]","IVMRWindowlessControl9 interface","IVMRWindowlessControl9 interface [DirectShow]","GetMaxIdealVideoSize method","IVMRWindowlessControl9.GetMaxIdealVideoSize","IVMRWindowlessControl9::GetMaxIdealVideoSize","IVMRWindowlessControl9GetMaxIdealVideoSize","dshow.ivmrwindowlesscontrol9_getmaxidealvideosize","vmr9/IVMRWindowlessControl9::GetMaxIdealVideoSize"]
old-location: dshow\ivmrwindowlesscontrol9_getmaxidealvideosize.htm
tech.root: dshow
ms.assetid: 0aac9c10-c152-4c26-b520-b4ccaf37600c
ms.date: 12/05/2018
ms.keywords: GetMaxIdealVideoSize, GetMaxIdealVideoSize method [DirectShow], GetMaxIdealVideoSize method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetMaxIdealVideoSize method, IVMRWindowlessControl9.GetMaxIdealVideoSize, IVMRWindowlessControl9::GetMaxIdealVideoSize, IVMRWindowlessControl9GetMaxIdealVideoSize, dshow.ivmrwindowlesscontrol9_getmaxidealvideosize, vmr9/IVMRWindowlessControl9::GetMaxIdealVideoSize
f1_keywords:
- vmr9/IVMRWindowlessControl9.GetMaxIdealVideoSize
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
- IVMRWindowlessControl9.GetMaxIdealVideoSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl9::GetMaxIdealVideoSize


## -description



The <code>GetMaxIdealVideoSize</code> method retrieves the maximum video size that the VMR can display without incurring significant performance or image quality degradation.




## -parameters




### -param lpWidth [out]

Pointer that receives the maximum ideal width.


### -param lpHeight [out]

Pointer that receives the maximum ideal height.


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




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getminidealvideosize">GetMinIdealVideoSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrwindowlesscontrol9">IVMRWindowlessControl9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

