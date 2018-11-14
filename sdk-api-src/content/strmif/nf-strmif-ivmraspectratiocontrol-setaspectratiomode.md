---
UID: NF:strmif.IVMRAspectRatioControl.SetAspectRatioMode
title: IVMRAspectRatioControl::SetAspectRatioMode
author: windows-sdk-content
description: The SetAspectRatioMode method specifies whether the VMR will preserve the aspect ratio of the source video.
old-location: dshow\ivmraspectratiocontrol_setaspectratiomode.htm
tech.root: DirectShow
ms.assetid: e73362ea-b153-4d25-b30e-c69274b49bf9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVMRAspectRatioControl interface [DirectShow],SetAspectRatioMode method, IVMRAspectRatioControl.SetAspectRatioMode, IVMRAspectRatioControl::SetAspectRatioMode, IVMRAspectRatioControlSetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [DirectShow], SetAspectRatioMode method [DirectShow],IVMRAspectRatioControl interface, dshow.ivmraspectratiocontrol_setaspectratiomode, strmif/IVMRAspectRatioControl::SetAspectRatioMode
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
 - IVMRAspectRatioControl.SetAspectRatioMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IVMRAspectRatioControl.SetAspectRatioMode
: 
---

# IVMRAspectRatioControl::SetAspectRatioMode


## -description



The <code>SetAspectRatioMode</code> method specifies whether the VMR will preserve the aspect ratio of the source video.




## -parameters




### -param dwARMode

TBD




#### - AspectRatioMode [in]

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a341be9d-9801-4215-840d-7d581e9ec3cb">IVMRAspectRatioControl Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

