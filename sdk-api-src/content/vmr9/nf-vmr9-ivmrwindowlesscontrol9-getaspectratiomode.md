---
UID: NF:vmr9.IVMRWindowlessControl9.GetAspectRatioMode
title: IVMRWindowlessControl9::GetAspectRatioMode (vmr9.h)
author: windows-sdk-content
description: The GetAspectRatioMode method retrieves the current aspect ratio display mode.
old-location: dshow\ivmrwindowlesscontrol9_getaspectratiomode.htm
tech.root: DirectShow
ms.assetid: c18ab567-5e0d-400a-8dc1-e9ad83650b7c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [DirectShow], GetAspectRatioMode method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetAspectRatioMode method, IVMRWindowlessControl9.GetAspectRatioMode, IVMRWindowlessControl9::GetAspectRatioMode, IVMRWindowlessControl9GetAspectRatioMode, dshow.ivmrwindowlesscontrol9_getaspectratiomode, vmr9/IVMRWindowlessControl9::GetAspectRatioMode
ms.topic: method
f1_keywords: 
 - "vmr9/IVMRWindowlessControl9.GetAspectRatioMode"
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
 - IVMRWindowlessControl9.GetAspectRatioMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl9::GetAspectRatioMode


## -description



The <code>GetAspectRatioMode</code> method retrieves the current aspect ratio display mode.




## -parameters




### -param lpAspectRatioMode [out]

Pointer to a DWORD that receives a <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/ne-vmr9-__midl___midl_itf_vmr9_0000_0004_0001">VMR9AspectRatioMode</a> value that indicates the current aspect ratio mode.


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




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrwindowlesscontrol9">IVMRWindowlessControl9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode">SetAspectRatioMode</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

