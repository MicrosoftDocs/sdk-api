---
UID: NF:vmr9.IVMRAspectRatioControl9.SetAspectRatioMode
title: IVMRAspectRatioControl9::SetAspectRatioMode
author: windows-sdk-content
description: The SetAspectRatioMode method specifies whether the VMR preserves the aspect ratio of the source video.
old-location: dshow\ivmraspectratiocontrol9_setaspectratiomode.htm
tech.root: DirectShow
ms.assetid: adc34013-a349-4cf6-b5c2-58b7b212d630
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRAspectRatioControl9 interface [DirectShow],SetAspectRatioMode method, IVMRAspectRatioControl9.SetAspectRatioMode, IVMRAspectRatioControl9::SetAspectRatioMode, IVMRAspectRatioControl9SetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [DirectShow], SetAspectRatioMode method [DirectShow],IVMRAspectRatioControl9 interface, dshow.ivmraspectratiocontrol9_setaspectratiomode, vmr9/IVMRAspectRatioControl9::SetAspectRatioMode
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
 - IVMRAspectRatioControl9.SetAspectRatioMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRAspectRatioControl9::SetAspectRatioMode


## -description



The <code>SetAspectRatioMode</code> method specifies whether the VMR preserves the aspect ratio of the source video.




## -parameters




### -param dwARMode [in]

Specifies a member of the <a href="https://msdn.microsoft.com/en-us/library/Dd390954(v=VS.85).aspx">VMR_ASPECT_RATIO_MODE</a> enumeration type.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377343(v=VS.85).aspx">IVMRAspectRatioControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

