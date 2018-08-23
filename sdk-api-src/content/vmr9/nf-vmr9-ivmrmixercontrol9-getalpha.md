---
UID: NF:vmr9.IVMRMixerControl9.GetAlpha
title: IVMRMixerControl9::GetAlpha
author: windows-sdk-content
description: The GetAlpha method retrieves the constant alpha value that is applied to this video stream.
old-location: dshow\ivmrmixercontrol9_getalpha.htm
old-project: DirectShow
ms.assetid: 0806f27c-4728-4492-a2ac-26067b7c0aaa
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetAlpha, GetAlpha method [DirectShow], GetAlpha method [DirectShow],IVMRMixerControl9 interface, IVMRMixerControl9 interface [DirectShow],GetAlpha method, IVMRMixerControl9.GetAlpha, IVMRMixerControl9::GetAlpha, IVMRMixerControl9GetAlpha, dshow.ivmrmixercontrol9_getalpha, vmr9/IVMRMixerControl9::GetAlpha
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
 - IVMRMixerControl9.GetAlpha
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRMixerControl9::GetAlpha


## -description



The <code>GetAlpha</code> method retrieves the constant alpha value that is applied to this video stream.




## -parameters




### -param dwStreamID [in]

Specifies the input stream. This value corresponds to the input pin. For example, the first input pin is stream 0.


### -param pAlpha [out]

Pointer to a variable that receives the current alpha value.


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
<i>pAlpha</i> is invalid.

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
 

 

