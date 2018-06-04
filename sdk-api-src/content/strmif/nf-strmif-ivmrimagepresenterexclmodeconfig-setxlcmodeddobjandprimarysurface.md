---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface


## -description



The <code>SetXlcModeDDObjAndPrimarySurface</code> method informs the VMR of the DirectDraw object and primary surface that were created by the application.




## -parameters




### -param lpDDObj [in]

Specifies the Exclusive Mode DirectDraw object created by the application.


### -param lpPrimarySurf [in]

Specifies the primary surface associated with the DirectDraw object.


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
</table>
 




## -remarks



The procedure for configuring and using an application-defined DirectDraw Exclusive Mode object is described in <a href="https://msdn.microsoft.com/3ef4f267-4dc2-421b-ade4-6b1efa364733">DirectDraw Exclusive Mode</a>.




## -see-also




<a href="https://msdn.microsoft.com/67c9675c-c0fd-44f6-bdeb-ac3f73e937cc">IVMRImagePresenterExclModeConfig Interface</a>



<a href="https://msdn.microsoft.com/09b756de-7fd2-44d8-9ef3-6b5dc56cb8b3">IVMRImagePresenterExclModeConfig::GetXlcModeDDObjAndPrimarySurface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

