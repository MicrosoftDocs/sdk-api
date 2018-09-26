---
UID: NF:vmr9.IVMRWindowlessControl9.GetVideoPosition
title: IVMRWindowlessControl9::GetVideoPosition
author: windows-sdk-content
description: The GetVideoPosition method retrieves the current source and destination rectangles used to display the video.
old-location: dshow\ivmrwindowlesscontrol9_getvideoposition.htm
tech.root: DirectShow
ms.assetid: 0963ec09-8637-441c-b10e-fecc11788e39
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetVideoPosition, GetVideoPosition method [DirectShow], GetVideoPosition method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetVideoPosition method, IVMRWindowlessControl9.GetVideoPosition, IVMRWindowlessControl9::GetVideoPosition, IVMRWindowlessControl9GetVideoPosition, dshow.ivmrwindowlesscontrol9_getvideoposition, vmr9/IVMRWindowlessControl9::GetVideoPosition
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVMRWindowlessControl9.GetVideoPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRWindowlessControl9::GetVideoPosition


## -description



The <code>GetVideoPosition</code> method retrieves the current source and destination rectangles used to display the video.




## -parameters




### -param lpSRCRect [out]

Pointer that receives the current source rectangle.


### -param lpDSTRect [out]

Pointer that receives the current destination rectangle.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

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
 




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9 Interface</a>



<a href="https://msdn.microsoft.com/9b165b51-c60d-4039-b652-5a5347dec224">SetVideoPosition</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

