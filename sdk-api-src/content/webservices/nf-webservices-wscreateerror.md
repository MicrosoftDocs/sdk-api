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

# WsCreateError function


## -description




                Creates an error object that can passed to functions to record rich error information.
            




## -parameters




### -param properties


                    An array of  <a href="https://msdn.microsoft.com/463b634f-bb15-494d-8061-c4fa0b97b990">WS_ERROR_PROPERTY</a> structures containing optional error properties.
                


### -param propertyCount [in]


                    The number of properties in the <i>properties</i> array.
                


### -param error

On success, a pointer that receives the address of the <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure representing the created error object.
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks




                When you no long need the error object, free it by calling  the <a href="https://msdn.microsoft.com/61da7bc2-b805-4379-a6b2-1e92374be1a0">WsFreeError</a> function.
            

By default, the
                language of any language-dependent information in the error object is  the current 
                user default UI language. However, you can change the language by setting 
                the WS_ERROR_PROPERTY_LANGID property. See the the <a href="https://msdn.microsoft.com/527e39be-c959-40db-8f0b-14dcd49a7ca7">WS_ERROR_PROPERTY_ID</a> enumeration.



