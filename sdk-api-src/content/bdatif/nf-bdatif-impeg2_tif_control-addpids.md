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

# IMPEG2_TIF_CONTROL::AddPIDs


## -description



The <b>AddPIDs</b> method tells the Network Provider which PIDs the TIF should receive.




## -parameters




### -param ulcPIDs [in]

Specifies the number of PIDs to add. This value must be equal to the number of elements in the array specified by <i>pulPIDs</i>.


### -param pulPIDs [in]

Specifies an array of PID values to add. The array must contain <i>ulcPIDs</i> elements.


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



Only the TIF knows which table sections it requires. It uses this method to tell the Network Provider the PIDs for the packets that contain those tables. The Network Provider forwards the information to the Demux, which immediately begins routing packets with the specified PIDs to the TIF.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9583365d-b318-49e2-a32f-f6cc9d3f289d">IMPEG2_TIF_CONTROL Interface</a>



<a href="https://msdn.microsoft.com/c7ca141b-e471-47ce-96b5-b2c0cad89daf">IMPEG2_TIF_CONTROL::GetPIDs</a>
 

 

