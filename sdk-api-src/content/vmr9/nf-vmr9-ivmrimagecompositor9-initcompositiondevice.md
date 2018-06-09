---
UID: NF:vmr9.IVMRImageCompositor9.InitCompositionDevice
title: IVMRImageCompositor9::InitCompositionDevice
author: windows-sdk-content
description: The InitCompositionDevice method informs the compositor that a new composition target has been created.
old-location: dshow\ivmrimagecompositor9_initcompositiondevice.htm
old-project: DirectShow
ms.assetid: 78381141-6b6d-4ed5-b8d3-aa1114fd9ac0
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IVMRImageCompositor9 interface [DirectShow],InitCompositionDevice method, IVMRImageCompositor9.InitCompositionDevice, IVMRImageCompositor9::InitCompositionDevice, IVMRImageCompositor9InitCompositionDevice, InitCompositionDevice, InitCompositionDevice method [DirectShow], InitCompositionDevice method [DirectShow],IVMRImageCompositor9 interface, dshow.ivmrimagecompositor9_initcompositiondevice, vmr9/IVMRImageCompositor9::InitCompositionDevice
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
 - IVMRImageCompositor9.InitCompositionDevice
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRImageCompositor9::InitCompositionDevice


## -description



The <code>InitCompositionDevice</code> method informs the compositor that a new composition target has been created. The compositor should perform any necessary configuration work in this method. This could include attaching a Z or stencil buffer for the new render target.




## -parameters




### -param pD3DDevice [in]

Pointer to the <b>IUnknown</b> interface of the Direct3D device object.


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
</table>
 




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/19fda7f2-000f-47d0-a7c7-d8421de418a2">IVMRImageCompositor9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

