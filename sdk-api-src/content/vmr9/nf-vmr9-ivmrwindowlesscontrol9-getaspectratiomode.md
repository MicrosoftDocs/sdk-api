---
UID: NF:vmr9.IVMRWindowlessControl9.GetAspectRatioMode
title: IVMRWindowlessControl9::GetAspectRatioMode method
author: windows-driver-content
description: The GetAspectRatioMode method retrieves the current aspect ratio display mode.
old-location: dshow\ivmrwindowlesscontrol9_getaspectratiomode.htm
old-project: DirectShow
ms.assetid: c18ab567-5e0d-400a-8dc1-e9ad83650b7c
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetAspectRatioMode method [DirectShow], GetAspectRatioMode method [DirectShow], IVMRWindowlessControl9 interface, GetAspectRatioMode,IVMRWindowlessControl9.GetAspectRatioMode, IVMRWindowlessControl9, IVMRWindowlessControl9 interface [DirectShow], GetAspectRatioMode method, IVMRWindowlessControl9::GetAspectRatioMode, IVMRWindowlessControl9GetAspectRatioMode, dshow.ivmrwindowlesscontrol9_getaspectratiomode, vmr9/IVMRWindowlessControl9::GetAspectRatioMode
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
-	IVMRWindowlessControl9.GetAspectRatioMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRWindowlessControl9::GetAspectRatioMode method


## -description



The <code>GetAspectRatioMode</code> method retrieves the current aspect ratio display mode.




## -parameters




### -param lpAspectRatioMode [out]

Pointer to a DWORD that receives a <a href="https://msdn.microsoft.com/745e7aad-a598-4be6-b28b-bb5969ef0c77">VMR9AspectRatioMode</a> value that indicates the current aspect ratio mode.


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




<a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9 Interface</a>



<a href="https://msdn.microsoft.com/5ba46490-0a82-495f-8742-d7a8efa95332">SetAspectRatioMode</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

