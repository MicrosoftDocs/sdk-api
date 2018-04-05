---
UID: NF:vmr9.IVMRMixerControl9.GetMixingPrefs
title: IVMRMixerControl9::GetMixingPrefs method
author: windows-driver-content
description: The GetMixingPrefs method retrieves the mixing preferences for the stream.
old-location: dshow\ivmrmixercontrol9_getmixingprefs.htm
old-project: DirectShow
ms.assetid: 25df0310-124a-48a5-b0fc-bea1dfd35781
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetMixingPrefs method [DirectShow], GetMixingPrefs method [DirectShow], IVMRMixerControl9 interface, GetMixingPrefs,IVMRMixerControl9.GetMixingPrefs, IVMRMixerControl9, IVMRMixerControl9 interface [DirectShow], GetMixingPrefs method, IVMRMixerControl9::GetMixingPrefs, IVMRMixerControl9GetMixingPrefs, dshow.ivmrmixercontrol9_getmixingprefs, vmr9/IVMRMixerControl9::GetMixingPrefs
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
-	IVMRMixerControl9.GetMixingPrefs
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRMixerControl9::GetMixingPrefs method


## -description



The <code>GetMixingPrefs</code> method retrieves the mixing preferences for the stream.




## -parameters




### -param pdwMixerPrefs [out]

Address of a variable that receives a bitwise OR combination of <a href="https://msdn.microsoft.com/59d3af89-248e-43cd-b6dc-e6c0a4d5f5fb">VMR9MixerPrefs</a> flags.


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



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

