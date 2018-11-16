---
UID: NF:strmif.IVMRWindowlessControl.GetVideoPosition
title: IVMRWindowlessControl::GetVideoPosition
author: windows-sdk-content
description: The GetVideoPosition method retrieves the current source and destination rectangles used to display the video.
old-location: dshow\ivmrwindowlesscontrol_getvideoposition.htm
tech.root: DirectShow
ms.assetid: 1d7f1a8b-bbc4-43ae-b8e6-410561087204
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetVideoPosition, GetVideoPosition method [DirectShow], GetVideoPosition method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetVideoPosition method, IVMRWindowlessControl.GetVideoPosition, IVMRWindowlessControl::GetVideoPosition, IVMRWindowlessControlGetVideoPosition, dshow.ivmrwindowlesscontrol_getvideoposition, strmif/IVMRWindowlessControl::GetVideoPosition
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
 - IVMRWindowlessControl.GetVideoPosition
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
- IVMRWindowlessControl.GetVideoPosition
: 
---

# IVMRWindowlessControl::GetVideoPosition


## -description



The <code>GetVideoPosition</code> method retrieves the current source and destination rectangles used to display the video.




## -parameters




### -param lpSRCRect [out]

Pointer that receives the current source rectangle.


### -param lpDSTRect [out]

Pointer that receives the current destination rectangle.


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



<a href="https://msdn.microsoft.com/3cf75b8e-850d-4514-9502-a71c801e0d92">IVMRWindowlessControl::SetVideoPosition</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

