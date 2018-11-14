---
UID: NF:strmif.IVMRWindowlessControl.GetColorKey
title: IVMRWindowlessControl::GetColorKey
author: windows-sdk-content
description: The GetColorKey method retrieves the current source color key value used by the VMR.
old-location: dshow\ivmrwindowlesscontrol_getcolorkey.htm
tech.root: DirectShow
ms.assetid: e10f9e03-fbcd-4002-babc-fb028e399d72
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetColorKey, GetColorKey method [DirectShow], GetColorKey method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetColorKey method, IVMRWindowlessControl.GetColorKey, IVMRWindowlessControl::GetColorKey, IVMRWindowlessControlGetColorKey, dshow.ivmrwindowlesscontrol_getcolorkey, strmif/IVMRWindowlessControl::GetColorKey
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVMRWindowlessControl.GetColorKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IVMRWindowlessControl.GetColorKey
: 
---

# IVMRWindowlessControl::GetColorKey


## -description



The <code>GetColorKey</code> method retrieves the current source color key value used by the VMR.




## -parameters




### -param lpClr [out]

Pointer to a <b>COLORREF</b> variable that receives the current color key value.


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



<a href="https://msdn.microsoft.com/9facf4af-ed56-4a94-b351-35ddd7f63e6e">IVMRWindowlessControl::SetColorKey</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

