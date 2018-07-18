---
UID: NF:vmr9.IVMRDeinterlaceControl9.GetDeinterlacePrefs
title: IVMRDeinterlaceControl9::GetDeinterlacePrefs
author: windows-sdk-content
description: The GetDeinterlacePrefs method queries how the VMR will select a deinterlacing mode if it cannot use the preferred deinterlacing mode.
old-location: dshow\ivmrdeinterlacecontrol9_getdeinterlaceprefs.htm
old-project: DirectShow
ms.assetid: 0ada3e78-f093-4b03-8db6-793cf80f0000
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetDeinterlacePrefs, GetDeinterlacePrefs method [DirectShow], GetDeinterlacePrefs method [DirectShow],IVMRDeinterlaceControl9 interface, IVMRDeinterlaceControl9 interface [DirectShow],GetDeinterlacePrefs method, IVMRDeinterlaceControl9.GetDeinterlacePrefs, IVMRDeinterlaceControl9::GetDeinterlacePrefs, IVMRDeinterlaceControl9GetDeinterlacePrefs, dshow.ivmrdeinterlacecontrol9_getdeinterlaceprefs, vmr9/IVMRDeinterlaceControl9::GetDeinterlacePrefs
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
 - IVMRDeinterlaceControl9.GetDeinterlacePrefs
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRDeinterlaceControl9::GetDeinterlacePrefs


## -description



The <b>GetDeinterlacePrefs</b> method queries how the VMR will select a deinterlacing mode if it cannot use the preferred deinterlacing mode.




## -parameters




### -param lpdwDeinterlacePrefs [in]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/1e5f5749-bdf9-4220-9867-ba6899797850">VMR9DeinterlacePrefs</a> enumeration.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

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



By default, the preferred deinterlacing mode is the first mode reported by the driver. The application can set the preferred mode by calling the <a href="https://msdn.microsoft.com/2c88b3b9-32eb-473b-9db5-9e9d65e2062c">IVMRDeinterlaceControl9::SetDeinterlaceMode</a> method. If the VMR cannot use the preferred mode, it will fall back to another mode as specified by the <i>dwDeinterlacePrefs</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/685f3627-30bd-4c78-9eda-0b06203dd46e">IVMRDeinterlaceControl9 Interface</a>



<a href="https://msdn.microsoft.com/31d59f17-552b-46d1-89e4-751216f54280">Setting Deinterlace Preferences</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a>
 

 

