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

# ILoadChangeContext::SetRecoverableErrorOnChangeUnit


## -description


Indicates that a recoverable error occurred when data for the specified change unit was loaded from the item store.


## -parameters




### -param hrError [in]

The error code that is associated with the error that prevented the change unit data from being loaded.


### -param pChangeUnit [in]

The change unit change that caused the error.


### -param pErrorData [in]

Additional information about the error.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>hrError</i> does not specify an error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ON_CREATE_MUST_FAIL_ENTIRE_ITEM</b></dt>
</dl>
</td>
<td width="60%">
The change that contains this change unit refers to an item creation. In this case, the error must be reported on the item change by using <a href="https://msdn.microsoft.com/9e557889-a4f6-4e05-99ce-bb05013dc4cd">ILoadChangeContext::SetRecoverableErrorOnChange</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
 An internal error has occurred.

</td>
</tr>
</table>
 




## -remarks



When this method is called, an <b>IChangeUnitException</b> object is added to the learned knowledge; and the change unit change will not be enumerated again for the duration of the synchronization session.





## -see-also




<a href="https://msdn.microsoft.com/3b47abab-0a33-405f-a765-307ab800bad6">IChangeUnitException Interface</a>



<a href="https://msdn.microsoft.com/11d8971b-354f-4347-9d3f-6d32df8dc9d2">ILoadChangeContext Interface</a>
 

 

