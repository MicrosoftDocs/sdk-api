---
UID: NF:vmr9.IVMRMixerControl9.GetMixingPrefs
title: IVMRMixerControl9::GetMixingPrefs (vmr9.h)
author: windows-sdk-content
description: The GetMixingPrefs method retrieves the mixing preferences for the stream.
old-location: dshow\ivmrmixercontrol9_getmixingprefs.htm
tech.root: DirectShow
ms.assetid: 25df0310-124a-48a5-b0fc-bea1dfd35781
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMixingPrefs, GetMixingPrefs method [DirectShow], GetMixingPrefs method [DirectShow],IVMRMixerControl9 interface, IVMRMixerControl9 interface [DirectShow],GetMixingPrefs method, IVMRMixerControl9.GetMixingPrefs, IVMRMixerControl9::GetMixingPrefs, IVMRMixerControl9GetMixingPrefs, dshow.ivmrmixercontrol9_getmixingprefs, vmr9/IVMRMixerControl9::GetMixingPrefs
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
 - IVMRMixerControl9.GetMixingPrefs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMixerControl9::GetMixingPrefs


## -description



The <code>GetMixingPrefs</code> method retrieves the mixing preferences for the stream.




## -parameters




### -param pdwMixerPrefs [out]

Address of a variable that receives a bitwise OR combination of <a href="https://msdn.microsoft.com/en-us/library/Dd407366(v=VS.85).aspx">VMR9MixerPrefs</a> flags.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd390457(v=VS.85).aspx">IVMRMixerControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

