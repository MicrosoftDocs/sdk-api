---
UID: NF:strmif.IVMRWindowlessControl.GetMinIdealVideoSize
title: IVMRWindowlessControl::GetMinIdealVideoSize
author: windows-sdk-content
description: The GetMinIdealVideoSize method retrieves the minimum video size that the VMR can display without incurring significant performance or image quality degradation.
old-location: dshow\ivmrwindowlesscontrol_getminidealvideosize.htm
old-project: DirectShow
ms.assetid: 602e32d4-41d6-4139-aa64-4b53caa50859
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetMinIdealVideoSize, GetMinIdealVideoSize method [DirectShow], GetMinIdealVideoSize method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetMinIdealVideoSize method, IVMRWindowlessControl.GetMinIdealVideoSize, IVMRWindowlessControl::GetMinIdealVideoSize, IVMRWindowlessControlGetMinIdealVideoSize, dshow.ivmrwindowlesscontrol_getminidealvideosize, strmif/IVMRWindowlessControl::GetMinIdealVideoSize
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRWindowlessControl.GetMinIdealVideoSize
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRWindowlessControl::GetMinIdealVideoSize


## -description



The <code>GetMinIdealVideoSize</code> method retrieves the minimum video size that the VMR can display without incurring significant performance or image quality degradation.




## -parameters




### -param lpWidth [out]

Pointer to a LONG value that receives the minimum ideal width.


### -param lpHeight [out]

Pointer to a LONG value that receives the minimum ideal height.


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



<a href="https://msdn.microsoft.com/1cfd8c4e-70e0-4a7e-a47e-4ad0535e5cb2">IVMRWindowlessControl::GetMaxIdealVideoSize</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

