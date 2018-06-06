---
UID: NF:strmif.IVMRWindowlessControl.GetMaxIdealVideoSize
title: IVMRWindowlessControl::GetMaxIdealVideoSize
author: windows-sdk-content
description: The GetMaxIdealVideoSize method retrieves the maximum video size that the VMR can display without incurring significant performance or image quality degradation.
old-location: dshow\ivmrwindowlesscontrol_getmaxidealvideosize.htm
old-project: DirectShow
ms.assetid: 1cfd8c4e-70e0-4a7e-a47e-4ad0535e5cb2
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetMaxIdealVideoSize, GetMaxIdealVideoSize method [DirectShow], GetMaxIdealVideoSize method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetMaxIdealVideoSize method, IVMRWindowlessControl.GetMaxIdealVideoSize, IVMRWindowlessControl::GetMaxIdealVideoSize, IVMRWindowlessControlGetMaxIdealVideoSize, dshow.ivmrwindowlesscontrol_getmaxidealvideosize, strmif/IVMRWindowlessControl::GetMaxIdealVideoSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRWindowlessControl.GetMaxIdealVideoSize
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRWindowlessControl::GetMaxIdealVideoSize


## -description



The <code>GetMaxIdealVideoSize</code> method retrieves the maximum video size that the VMR can display without incurring significant performance or image quality degradation.




## -parameters




### -param lpWidth [out]

Pointer that receives the maximum ideal width.


### -param lpHeight [out]

Pointer that receives the maximum ideal height.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl Interface</a>



<a href="https://msdn.microsoft.com/602e32d4-41d6-4139-aa64-4b53caa50859">IVMRWindowlessControl::GetMinIdealVideoSize</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

