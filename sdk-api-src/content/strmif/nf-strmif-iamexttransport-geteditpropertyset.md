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

# IAMExtTransport::GetEditPropertySet


## -description



The <code>GetEditPropertySet</code> method retrieves the state of an edit event.



This method is not implemented.


## -parameters




### -param EditID [in]

Specifies the edit property set. Use the identifier returned by the <a href="https://msdn.microsoft.com/40695c7c-7381-44c0-b41f-7c838c9c83b5">IAMExtTransport::SetEditPropertySet</a> method.


### -param pState [out]

Pointer to a <b>long</b> integer that receives the state of the edit property set:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>ED_ACTIVE</td>
<td>The edit property set is active.</td>
</tr>
<tr>
<td>ED_DELETE</td>
<td>The edit property set was deleted.</td>
</tr>
<tr>
<td>ED_INACTIVE</td>
<td>The edit property set is inactive.</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/40695c7c-7381-44c0-b41f-7c838c9c83b5">IAMExtTransport::SetEditPropertySet</a>
 

 

