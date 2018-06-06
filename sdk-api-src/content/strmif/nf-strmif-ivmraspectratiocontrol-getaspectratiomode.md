---
UID: NF:strmif.IVMRAspectRatioControl.GetAspectRatioMode
title: IVMRAspectRatioControl::GetAspectRatioMode
author: windows-sdk-content
description: The GetAspectRatioMode method queries whether the VMR will preserve the aspect ratio of the source video.
old-location: dshow\ivmraspectratiocontrol_getaspectratiomode.htm
old-project: DirectShow
ms.assetid: baecb2a1-e7d8-43ee-ac7d-d2dcf50cb594
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [DirectShow], GetAspectRatioMode method [DirectShow],IVMRAspectRatioControl interface, IVMRAspectRatioControl interface [DirectShow],GetAspectRatioMode method, IVMRAspectRatioControl.GetAspectRatioMode, IVMRAspectRatioControl::GetAspectRatioMode, IVMRAspectRatioControlGetAspectRatioMode, dshow.ivmraspectratiocontrol_getaspectratiomode, strmif/IVMRAspectRatioControl::GetAspectRatioMode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRAspectRatioControl.GetAspectRatioMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRAspectRatioControl::GetAspectRatioMode


## -description



The <code>GetAspectRatioMode</code> method queries whether the VMR will preserve the aspect ratio of the source video.




## -parameters




### -param lpdwARMode






#### - lpAspectRatioMode [out]

Pointer to a variable that receives a <a href="https://msdn.microsoft.com/dd1d1d99-008b-4234-a38a-314ba02bb116">VMR_ASPECT_RATIO_MODE</a> value indicating the aspect ratio mode.


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



<a href="https://msdn.microsoft.com/a341be9d-9801-4215-840d-7d581e9ec3cb">IVMRAspectRatioControl Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

