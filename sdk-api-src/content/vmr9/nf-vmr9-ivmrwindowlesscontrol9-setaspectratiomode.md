---
UID: NF:vmr9.IVMRWindowlessControl9.SetAspectRatioMode
title: IVMRWindowlessControl9::SetAspectRatioMode
author: windows-sdk-content
description: The SetAspectRatioMode method sets the current aspect ratio display mode.
old-location: dshow\ivmrwindowlesscontrol9_setaspectratiomode.htm
old-project: DirectShow
ms.assetid: 5ba46490-0a82-495f-8742-d7a8efa95332
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IVMRWindowlessControl9 interface [DirectShow],SetAspectRatioMode method, IVMRWindowlessControl9.SetAspectRatioMode, IVMRWindowlessControl9::SetAspectRatioMode, IVMRWindowlessControl9SetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [DirectShow], SetAspectRatioMode method [DirectShow],IVMRWindowlessControl9 interface, dshow.ivmrwindowlesscontrol9_setaspectratiomode, vmr9/IVMRWindowlessControl9::SetAspectRatioMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vmr9.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VMR9DeinterlaceTech
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRWindowlessControl9.SetAspectRatioMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRWindowlessControl9::SetAspectRatioMode


## -description



The <code>SetAspectRatioMode</code> method sets the current aspect ratio display mode.




## -parameters




### -param AspectRatioMode [in]

A <a href="https://msdn.microsoft.com/745e7aad-a598-4be6-b28b-bb5969ef0c77">VMR9AspectRatioMode</a> value that specifies the aspect ratio mode.


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




<a href="https://msdn.microsoft.com/c18ab567-5e0d-400a-8dc1-e9ad83650b7c">GetAspectRatioMode</a>



<a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

