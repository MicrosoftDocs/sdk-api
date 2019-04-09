---
UID: NF:vmr9.IVMRDeinterlaceControl9.SetDeinterlacePrefs
title: IVMRDeinterlaceControl9::SetDeinterlacePrefs (vmr9.h)
author: windows-sdk-content
description: The SetDeinterlacePrefs method specifies how the VMR will select a deinterlacing mode if it cannot use the preferred deinterlacing mode.
old-location: dshow\ivmrdeinterlacecontrol9_setdeinterlaceprefs.htm
tech.root: DirectShow
ms.assetid: 5d5b450f-bb87-41a2-bbb1-06b3956ba225
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRDeinterlaceControl9 interface [DirectShow],SetDeinterlacePrefs method, IVMRDeinterlaceControl9.SetDeinterlacePrefs, IVMRDeinterlaceControl9::SetDeinterlacePrefs, IVMRDeinterlaceControl9SetDeinterlacePrefs, SetDeinterlacePrefs, SetDeinterlacePrefs method [DirectShow], SetDeinterlacePrefs method [DirectShow],IVMRDeinterlaceControl9 interface, dshow.ivmrdeinterlacecontrol9_setdeinterlaceprefs, vmr9/IVMRDeinterlaceControl9::SetDeinterlacePrefs
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
 - IVMRDeinterlaceControl9.SetDeinterlacePrefs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRDeinterlaceControl9::SetDeinterlacePrefs


## -description



The <b>SetDeinterlacePrefs</b> method specifies how the VMR will select a deinterlacing mode if it cannot use the preferred deinterlacing mode.




## -parameters




### -param dwDeinterlacePrefs [in]

Specifies a member of the <a href="https://msdn.microsoft.com/en-us/library/Dd407363(v=VS.85).aspx">VMR9DeinterlacePrefs</a> enumeration type.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_VMR_NOT_IN_MIXER_MODE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in mixer mode.

</td>
</tr>
</table>
 




## -remarks



By default, the preferred deinterlacing mode is the first mode reported by the driver. The application can set the preferred mode by calling the <a href="https://msdn.microsoft.com/en-us/library/Dd377355(v=VS.85).aspx">IVMRDeinterlaceControl9::SetDeinterlaceMode</a> method. If the VMR cannot use the preferred mode, it will fall back to another mode as specified by the <i>dwDeinterlacePrefs</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377349(v=VS.85).aspx">IVMRDeinterlaceControl9 Interface</a>



<a href="https://msdn.microsoft.com/31d59f17-552b-46d1-89e4-751216f54280">Setting Deinterlace Preferences</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a>
 

 

