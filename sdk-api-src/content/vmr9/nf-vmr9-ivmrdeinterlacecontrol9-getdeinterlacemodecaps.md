---
UID: NF:vmr9.IVMRDeinterlaceControl9.GetDeinterlaceModeCaps
title: IVMRDeinterlaceControl9::GetDeinterlaceModeCaps
author: windows-sdk-content
description: The GetDeinterlaceModeCaps method gets the capabilities of a deinterlacing mode supported by the graphics device driver.
old-location: dshow\ivmrdeinterlacecontrol9_getdeinterlacemodecaps.htm
old-project: DirectShow
ms.assetid: 62b71df5-7665-4023-90cd-e426b751c1df
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetDeinterlaceModeCaps, GetDeinterlaceModeCaps method [DirectShow], GetDeinterlaceModeCaps method [DirectShow],IVMRDeinterlaceControl9 interface, IVMRDeinterlaceControl9 interface [DirectShow],GetDeinterlaceModeCaps method, IVMRDeinterlaceControl9.GetDeinterlaceModeCaps, IVMRDeinterlaceControl9::GetDeinterlaceModeCaps, IVMRDeinterlaceControl9GetDeinterlaceModeCaps, dshow.ivmrdeinterlacecontrol9_getdeinterlacemodecaps, vmr9/IVMRDeinterlaceControl9::GetDeinterlaceModeCaps
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
-	IVMRDeinterlaceControl9.GetDeinterlaceModeCaps
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRDeinterlaceControl9::GetDeinterlaceModeCaps


## -description



The <b>GetDeinterlaceModeCaps</b> method gets the capabilities of a deinterlacing mode supported by the graphics device driver.




## -parameters




### -param lpDeinterlaceMode [in]


            Pointer to a GUID that identifies the deinterlacing mode. Call the <a href="https://msdn.microsoft.com/5d7d72f3-140c-4af4-8876-80a558575a57">IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes</a> method to obtain a list of GUIDs supported by the driver.
          


### -param lpVideoDescription [in]


            Pointer to a <a href="https://msdn.microsoft.com/af4bf46a-fae7-4485-b5fb-3fd1857f383f">VMR9VideoDesc</a> structure describing the video to deinterlace.
          Set the <b>dwSize</b> member of the structure before calling the method. 


### -param lpDeinterlaceCaps [out]


            Pointer to a <a href="https://msdn.microsoft.com/ae71c9d6-2540-4679-927c-e1d759df7009">VMR9DeinterlaceCaps</a> structure. Set the <b>dwSize</b> member of the structure before calling the method. The method fills the structure with information about the specified deinterlacing mode.
          


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
<dt><b>VFW_E_DDRAW_CAPS_NOT_SUITABLE</b></dt>
</dl>
</td>
<td width="60%">
The video card does not support hardware deinterlacing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_VMR_NO_DEINTERLACE_HW</b></dt>
</dl>
</td>
<td width="60%">
The video card does not support hardware deinterlacing.

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



The method returns <b>E_INVALIDARG</b> if you do not set the <b>dwSize</b> member in the <a href="https://msdn.microsoft.com/af4bf46a-fae7-4485-b5fb-3fd1857f383f">VMR9VideoDesc</a> and <a href="https://msdn.microsoft.com/ae71c9d6-2540-4679-927c-e1d759df7009">VMR9DeinterlaceCaps</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/685f3627-30bd-4c78-9eda-0b06203dd46e">IVMRDeinterlaceControl9 Interface</a>



<a href="https://msdn.microsoft.com/31d59f17-552b-46d1-89e4-751216f54280">Setting Deinterlace Preferences</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a>
 

 

