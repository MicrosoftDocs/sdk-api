---
UID: NF:vmr9.IVMRWindowlessControl9.GetMinIdealVideoSize
title: IVMRWindowlessControl9::GetMinIdealVideoSize
author: windows-sdk-content
description: The GetMinIdealVideoSize method retrieves the minimum video size that the VMR can display without incurring significant performance or image quality degradation.
old-location: dshow\ivmrwindowlesscontrol9_getminidealvideosize.htm
tech.root: DirectShow
ms.assetid: 9e100f04-28fc-4449-9fe4-0f0074e6439c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetMinIdealVideoSize, GetMinIdealVideoSize method [DirectShow], GetMinIdealVideoSize method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetMinIdealVideoSize method, IVMRWindowlessControl9.GetMinIdealVideoSize, IVMRWindowlessControl9::GetMinIdealVideoSize, IVMRWindowlessControl9GetMinIdealVideoSize, dshow.ivmrwindowlesscontrol9_getminidealvideosize, vmr9/IVMRWindowlessControl9::GetMinIdealVideoSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IVMRWindowlessControl9.GetMinIdealVideoSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/0aac9c10-c152-4c26-b520-b4ccaf37600c">GetMaxIdealVideoSize</a>



<a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

