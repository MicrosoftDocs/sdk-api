---
UID: NF:strmif.IVMRWindowlessControl.SetColorKey
title: IVMRWindowlessControl::SetColorKey
author: windows-sdk-content
description: The SetColorKey method sets the source color key value that the VMR should use.
old-location: dshow\ivmrwindowlesscontrol_setcolorkey.htm
old-project: DirectShow
ms.assetid: 9facf4af-ed56-4a94-b351-35ddd7f63e6e
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IVMRWindowlessControl interface [DirectShow],SetColorKey method, IVMRWindowlessControl.SetColorKey, IVMRWindowlessControl::SetColorKey, IVMRWindowlessControlSetColorKey, SetColorKey, SetColorKey method [DirectShow], SetColorKey method [DirectShow],IVMRWindowlessControl interface, dshow.ivmrwindowlesscontrol_setcolorkey, strmif/IVMRWindowlessControl::SetColorKey
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
 - IVMRWindowlessControl.SetColorKey
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRWindowlessControl::SetColorKey


## -description



The <code>SetColorKey</code> method sets the source color key value that the VMR should use.




## -parameters




### -param Clr [in]

Specifies the source color key.


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
 




## -remarks



Color key control is only meaningful when the VMR is using an overlay surface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl Interface</a>



<a href="https://msdn.microsoft.com/e10f9e03-fbcd-4002-babc-fb028e399d72">IVMRWindowlessControl::GetColorKey</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

