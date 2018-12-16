---
UID: NF:vmr9.IVMRWindowlessControl9.SetAspectRatioMode
title: IVMRWindowlessControl9::SetAspectRatioMode
author: windows-sdk-content
description: The SetAspectRatioMode method sets the current aspect ratio display mode.
old-location: dshow\ivmrwindowlesscontrol9_setaspectratiomode.htm
tech.root: DirectShow
ms.assetid: 5ba46490-0a82-495f-8742-d7a8efa95332
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRWindowlessControl9 interface [DirectShow],SetAspectRatioMode method, IVMRWindowlessControl9.SetAspectRatioMode, IVMRWindowlessControl9::SetAspectRatioMode, IVMRWindowlessControl9SetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [DirectShow], SetAspectRatioMode method [DirectShow],IVMRWindowlessControl9 interface, dshow.ivmrwindowlesscontrol9_setaspectratiomode, vmr9/IVMRWindowlessControl9::SetAspectRatioMode
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
 - IVMRWindowlessControl9.SetAspectRatioMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRWindowlessControl9::SetAspectRatioMode


## -description



The <code>SetAspectRatioMode</code> method sets the current aspect ratio display mode.




## -parameters




### -param AspectRatioMode [in]

A <a href="https://msdn.microsoft.com/en-us/library/Dd407361(v=VS.85).aspx">VMR9AspectRatioMode</a> value that specifies the aspect ratio mode.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd390539(v=VS.85).aspx">GetAspectRatioMode</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390537(v=VS.85).aspx">IVMRWindowlessControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

