---
UID: NF:vmr9.IVMRWindowlessControl9.GetMaxIdealVideoSize
title: IVMRWindowlessControl9::GetMaxIdealVideoSize
author: windows-sdk-content
description: The GetMaxIdealVideoSize method retrieves the maximum video size that the VMR can display without incurring significant performance or image quality degradation.
old-location: dshow\ivmrwindowlesscontrol9_getmaxidealvideosize.htm
old-project: DirectShow
ms.assetid: 0aac9c10-c152-4c26-b520-b4ccaf37600c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetMaxIdealVideoSize, GetMaxIdealVideoSize method [DirectShow], GetMaxIdealVideoSize method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetMaxIdealVideoSize method, IVMRWindowlessControl9.GetMaxIdealVideoSize, IVMRWindowlessControl9::GetMaxIdealVideoSize, IVMRWindowlessControl9GetMaxIdealVideoSize, dshow.ivmrwindowlesscontrol9_getmaxidealvideosize, vmr9/IVMRWindowlessControl9::GetMaxIdealVideoSize
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: VMR9DeinterlaceTech
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRWindowlessControl9.GetMaxIdealVideoSize
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
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




<a href="https://msdn.microsoft.com/9e100f04-28fc-4449-9fe4-0f0074e6439c">GetMinIdealVideoSize</a>



<a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

