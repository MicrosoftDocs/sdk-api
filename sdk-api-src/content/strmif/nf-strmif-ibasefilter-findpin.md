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

# IBaseFilter::FindPin


## -description



The <code>FindPin</code> method retrieves the pin with the specified identifier.




## -parameters




### -param Id [in]

Pointer to a constant wide-character string that identifies the pin. Call the <a href="https://msdn.microsoft.com/d4fb2713-549d-4c0d-9768-386bcffd696f">IPin::QueryId</a> method to retrieve a pin's identifier.


### -param ppPin [out]

Address of a variable that receives a pointer to the pin's <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface. If the method fails, <i>*ppPin</i> is set to <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Could not find a pin with this identifier.

</td>
</tr>
</table>
 




## -remarks



This method supports graph persistence. Use the <a href="https://msdn.microsoft.com/d4fb2713-549d-4c0d-9768-386bcffd696f">IPin::QueryId</a> method to save a pin's state, and use this method to restore the state. The pin's identifier string is defined by the filter implementation. The identifier must be unique within the filter.

If the method succeeds, the <b>IPin</b> interface that it returns has an outstanding reference count. Be sure to release the interface when you are done.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter Interface</a>
 

 

