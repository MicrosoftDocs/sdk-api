---
UID: NF:strmif.IVMRWindowlessControl.GetAspectRatioMode
title: IVMRWindowlessControl::GetAspectRatioMode
author: windows-driver-content
description: The GetAspectRatioMode method queries whether the VMR will preserve the aspect ratio of the source video.
old-location: dshow\ivmrwindowlesscontrol_getaspectratiomode.htm
old-project: DirectShow
ms.assetid: 452837f9-e910-4e6b-8552-9da29a6b63f1
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [DirectShow], GetAspectRatioMode method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetAspectRatioMode method, IVMRWindowlessControl.GetAspectRatioMode, IVMRWindowlessControl::GetAspectRatioMode, IVMRWindowlessControlGetAspectRatioMode, dshow.ivmrwindowlesscontrol_getaspectratiomode, strmif/IVMRWindowlessControl::GetAspectRatioMode
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
-	IVMRWindowlessControl.GetAspectRatioMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRWindowlessControl::GetAspectRatioMode


## -description



The <code>GetAspectRatioMode</code> method queries whether the VMR will preserve the aspect ratio of the source video.




## -parameters




### -param lpAspectRatioMode [out]

Pointer to a variable that receives a <a href="https://msdn.microsoft.com/dd1d1d99-008b-4234-a38a-314ba02bb116">VMR_ASPECT_RATIO_MODE</a> value indicating the aspect ratio mode.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.

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
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl Interface</a>



<a href="https://msdn.microsoft.com/421910fb-8007-4347-a57c-6a46b7b733b3">IVMRWindowlessControl::SetAspectRatioMode</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

