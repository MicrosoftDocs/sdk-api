---
UID: NF:vmr9.IVMRMixerControl9.GetBackgroundClr
title: IVMRMixerControl9::GetBackgroundClr
author: windows-sdk-content
description: The GetBackgroundClr method gets the current background color on the output rectangle.
old-location: dshow\ivmrmixercontrol9_getbackgroundclr.htm
tech.root: DirectShow
ms.assetid: 1be2fb34-b0f3-4dff-8813-a487229af6dc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBackgroundClr, GetBackgroundClr method [DirectShow], GetBackgroundClr method [DirectShow],IVMRMixerControl9 interface, IVMRMixerControl9 interface [DirectShow],GetBackgroundClr method, IVMRMixerControl9.GetBackgroundClr, IVMRMixerControl9::GetBackgroundClr, IVMRMixerControl9GetBackgroundClr, dshow.ivmrmixercontrol9_getbackgroundclr, vmr9/IVMRMixerControl9::GetBackgroundClr
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
 - IVMRMixerControl9.GetBackgroundClr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMixerControl9::GetBackgroundClr


## -description



The <code>GetBackgroundClr</code> method gets the current background color on the output rectangle.




## -parameters




### -param lpClrBkg [in]

Pointer to a variable that receives the background color.


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




<a href="https://msdn.microsoft.com/f311303a-8270-40b6-8153-e0bd8b232c69">IVMRMixerControl9 Interface</a>



<a href="https://msdn.microsoft.com/fed7f4bb-519c-4e02-be99-065b9131e57c">SetBackgroundClr</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

