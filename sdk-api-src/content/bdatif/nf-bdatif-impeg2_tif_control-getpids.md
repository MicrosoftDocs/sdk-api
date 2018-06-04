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

# IMPEG2_TIF_CONTROL::GetPIDs


## -description



The <b>GetPIDs</b> method retrieves the list of MPEG-2 Packet IDs being filtered into the TIF's input data.




## -parameters




### -param pulcPIDs [out]

Pointer to a variable that receives the number of PIDs that were retrieved.


### -param pulPIDs [out]

Pointer to a variable that receives an array of returned <b>ULONG</b> values representing the PID values. The number of elements in the array is equal to the value of <i>pulcPIDs</i>.


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



A custom TIF extension might or might not have need for this method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9583365d-b318-49e2-a32f-f6cc9d3f289d">IMPEG2_TIF_CONTROL Interface</a>



<a href="https://msdn.microsoft.com/27add7cc-1d77-4ac5-b63f-757f63f4c9b8">IMPEG2_TIF_CONTROL::AddPIDs</a>



<a href="https://msdn.microsoft.com/2d77c3d8-b91c-43de-b4c1-bd41636eb4ad">IMPEG2_TIF_CONTROL::GetPIDCount</a>
 

 

