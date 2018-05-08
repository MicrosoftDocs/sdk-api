---
UID: NF:strmif.IVMRWindowlessControl.SetAspectRatioMode
title: IVMRWindowlessControl::SetAspectRatioMode
author: windows-driver-content
description: The SetAspectRatioMode method specifies whether the VMR will preserve the aspect ratio of the source video.
old-location: dshow\ivmrwindowlesscontrol_setaspectratiomode.htm
old-project: DirectShow
ms.assetid: 421910fb-8007-4347-a57c-6a46b7b733b3
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IVMRWindowlessControl interface [DirectShow],SetAspectRatioMode method, IVMRWindowlessControl.SetAspectRatioMode, IVMRWindowlessControl::SetAspectRatioMode, IVMRWindowlessControlSetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [DirectShow], SetAspectRatioMode method [DirectShow],IVMRWindowlessControl interface, dshow.ivmrwindowlesscontrol_setaspectratiomode, strmif/IVMRWindowlessControl::SetAspectRatioMode
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
-	IVMRWindowlessControl.SetAspectRatioMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRWindowlessControl::SetAspectRatioMode


## -description



The <code>SetAspectRatioMode</code> method specifies whether the VMR will preserve the aspect ratio of the source video.




## -parameters




### -param AspectRatioMode [in]

Specifies a member of the <a href="https://msdn.microsoft.com/dd1d1d99-008b-4234-a38a-314ba02bb116">VMR_ASPECT_RATIO_MODE</a> enumeration type.


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
Invalid argument

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in windowless mode.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl Interface</a>



<a href="https://msdn.microsoft.com/452837f9-e910-4e6b-8552-9da29a6b63f1">IVMRWindowlessControl::GetAspectRatioMode</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

