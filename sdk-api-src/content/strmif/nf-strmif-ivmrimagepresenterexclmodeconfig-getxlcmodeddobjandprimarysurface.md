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

# IVMRImagePresenterExclModeConfig::GetXlcModeDDObjAndPrimarySurface


## -description



The <code>GetXlcModeDDObjAndPrimarySurface</code> method retrieves the DirectDraw object and primary surface currently being used by a VMR that has been configured for DirectDraw Exclusive Mode using the <b>SetXlcModeDDObjAndPrimarySurface</b> method.




## -parameters




### -param lpDDObj [out]

Retrieves the Exclusive Mode DirectDraw object created by the application.


### -param lpPrimarySurf [out]

Retrieves the primary surface associated with the DirectDraw object.


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



<a href="https://msdn.microsoft.com/3af69975-fe3c-45e6-b1f5-ce2dbda9a4dc">IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

