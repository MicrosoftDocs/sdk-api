---
UID: NF:vmr9.IVMRMixerControl9.SetZOrder
title: IVMRMixerControl9::SetZOrder
author: windows-sdk-content
description: The SetZOrder method sets this video stream's position in the Z-order; larger values are further away.
old-location: dshow\ivmrmixercontrol9_setzorder.htm
old-project: DirectShow
ms.assetid: fbc847d4-5d93-4994-b5f4-d753a528532a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IVMRMixerControl9 interface [DirectShow],SetZOrder method, IVMRMixerControl9.SetZOrder, IVMRMixerControl9::SetZOrder, IVMRMixerControl9SetZOrder, SetZOrder, SetZOrder method [DirectShow], SetZOrder method [DirectShow],IVMRMixerControl9 interface, dshow.ivmrmixercontrol9_setzorder, vmr9/IVMRMixerControl9::SetZOrder
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
 - IVMRMixerControl9.SetZOrder
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRMixerControl9::SetZOrder


## -description



The <code>SetZOrder</code> method sets this video stream's position in the Z-order; larger values are further away.




## -parameters




### -param dwStreamID [in]

Specifies the input stream. This value corresponds to the input pin. For example, the first input pin is stream 0.


### -param dwZ [in]

Double word containing the stream's position within the Z-order.


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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is not connected.

</td>
</tr>
</table>
 




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/f311303a-8270-40b6-8153-e0bd8b232c69">IVMRMixerControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

