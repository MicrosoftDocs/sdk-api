---
UID: NF:strmif.IVMRDeinterlaceControl.GetDeinterlaceModeCaps
title: IVMRDeinterlaceControl::GetDeinterlaceModeCaps method
author: windows-driver-content
description: The GetDeinterlaceModeCaps method retrieves the capabilities of a specific deinterlacing mode supported by the graphics device driver.
old-location: dshow\ivmrdeinterlacecontrol_getdeinterlacemodecaps.htm
old-project: DirectShow
ms.assetid: e672f3d4-1009-4c4c-bb1a-08f78c128423
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetDeinterlaceModeCaps method [DirectShow], GetDeinterlaceModeCaps method [DirectShow], IVMRDeinterlaceControl interface, GetDeinterlaceModeCaps,IVMRDeinterlaceControl.GetDeinterlaceModeCaps, IVMRDeinterlaceControl, IVMRDeinterlaceControl interface [DirectShow], GetDeinterlaceModeCaps method, IVMRDeinterlaceControl::GetDeinterlaceModeCaps, IVMRDeinterlaceControlGetDeinterlaceModeCaps, dshow.ivmrdeinterlacecontrol_getdeinterlacemodecaps, strmif/IVMRDeinterlaceControl::GetDeinterlaceModeCaps
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRDeinterlaceControl.GetDeinterlaceModeCaps
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRDeinterlaceControl::GetDeinterlaceModeCaps method


## -description


The <b>GetDeinterlaceModeCaps</b> method retrieves the capabilities of a specific deinterlacing mode supported by the graphics device driver.


## -parameters




### -param lpDeinterlaceMode [in]


            Pointer to a GUID that identifies the deinterlacing mode. Call the <a href="https://msdn.microsoft.com/0e6abb00-95fb-453d-9427-178058b217b8">GetNumberOfDeinterlaceModes</a> method to obtain a list of GUIDs supported by the driver.
          


### -param lpVideoDescription [in]


            Pointer to a <a href="https://msdn.microsoft.com/b02683ec-9bf9-4a69-87fb-d37a98f02e61">VMRVideoDesc</a> structure describing the video to deinterlace. Set the <b>dwSize</b> member of the structure before calling the method. 


### -param lpDeinterlaceCaps [out]

Pointer to a <a href="https://msdn.microsoft.com/e6152130-d574-4c9e-9d35-a42de709f9ae">VMRDeinterlaceCaps</a> structure. Set the <b>dwSize</b> member of the structure before calling the method. The method fills the structure with information about the specified deinterlacing mode.


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



The method returns <b>E_INVALIDARG</b> if you do not set the <b>dwSize</b> member in the <a href="https://msdn.microsoft.com/b02683ec-9bf9-4a69-87fb-d37a98f02e61">VMRVideoDesc</a> and <a href="https://msdn.microsoft.com/e6152130-d574-4c9e-9d35-a42de709f9ae">VMRDeinterlaceCaps</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/77abbcd4-6538-491d-b3c2-6a29a391c68a">IVMRDeinterlaceControl Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

