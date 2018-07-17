---
UID: NF:vmr9.IVMRAspectRatioControl9.GetAspectRatioMode
title: IVMRAspectRatioControl9::GetAspectRatioMode
author: windows-sdk-content
description: The GetAspectRatioMode method queries whether the VMR preserves the aspect ratio of the source video.
old-location: dshow\ivmraspectratiocontrol9_getaspectratiomode.htm
old-project: DirectShow
ms.assetid: e53e9015-5186-4807-a5ee-af8598a89a2b
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [DirectShow], GetAspectRatioMode method [DirectShow],IVMRAspectRatioControl9 interface, IVMRAspectRatioControl9 interface [DirectShow],GetAspectRatioMode method, IVMRAspectRatioControl9.GetAspectRatioMode, IVMRAspectRatioControl9::GetAspectRatioMode, IVMRAspectRatioControl9GetAspectRatioMode, dshow.ivmraspectratiocontrol9_getaspectratiomode, vmr9/IVMRAspectRatioControl9::GetAspectRatioMode
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
 - IVMRAspectRatioControl9.GetAspectRatioMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRAspectRatioControl9::GetAspectRatioMode


## -description



The <code>GetAspectRatioMode</code> method queries whether the VMR preserves the aspect ratio of the source video.




## -parameters




### -param lpdwARMode






#### - lpAspectRatioMode [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/dd1d1d99-008b-4234-a38a-314ba02bb116">VMR_ASPECT_RATIO_MODE</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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



<a href="https://msdn.microsoft.com/ae850eea-c283-4500-baa0-e26641576852">IVMRAspectRatioControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

