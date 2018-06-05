---
UID: NF:vmr9.IVMRWindowlessControl9.SetVideoPosition
title: IVMRWindowlessControl9::SetVideoPosition
author: windows-sdk-content
description: The SetVideoPosition method sets the source and destination rectangles for the video.
old-location: dshow\ivmrwindowlesscontrol9_setvideoposition.htm
old-project: DirectShow
ms.assetid: 9b165b51-c60d-4039-b652-5a5347dec224
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVMRWindowlessControl9 interface [DirectShow],SetVideoPosition method, IVMRWindowlessControl9.SetVideoPosition, IVMRWindowlessControl9::SetVideoPosition, IVMRWindowlessControl9SetVideoPosition, SetVideoPosition, SetVideoPosition method [DirectShow], SetVideoPosition method [DirectShow],IVMRWindowlessControl9 interface, dshow.ivmrwindowlesscontrol9_setvideoposition, vmr9/IVMRWindowlessControl9::SetVideoPosition
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRWindowlessControl9.SetVideoPosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRWindowlessControl9::SetVideoPosition


## -description



The <code>SetVideoPosition</code> method sets the source and destination rectangles for the video.




## -parameters




### -param lpSRCRect [in]

Pointer to a <b>RECT</b> structure that specifies the source rectangle. If <b>NULL</b>, the source rectangle does not change. The default source rectangle is the entire video image.


### -param lpDSTRect [in]

Pointer to a <b>RECT</b> structure that specifies the destination rectangle. If <b>NULL</b>, the destination rectangle does not change. The default destination rectangle is {0, 0, 0, 0}.


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



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

