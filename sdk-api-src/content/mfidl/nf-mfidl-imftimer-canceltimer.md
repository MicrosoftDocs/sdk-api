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

# IMFTimer::CancelTimer


## -description



Cancels a timer that was set using the <a href="https://msdn.microsoft.com/3b583541-6480-490d-883f-376ea95f7a98">IMFTimer::SetTimer</a> method.




## -parameters




### -param punkKey [in]

Pointer to the <b>IUnknown</b> interface that was returned in the <i>ppunkKey</i> parameter of the <a href="https://msdn.microsoft.com/3b583541-6480-490d-883f-376ea95f7a98">SetTimer</a> method.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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



Because the timer is dispatched asynchronously, the application's timer callback might get invoked even if this method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/152594df-de3d-4f6f-9277-dba95ab3533a">IMFTimer</a>
 

 

