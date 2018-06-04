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

# RpcMgmtEpEltInqNextW function


## -description


The 
<b>RpcMgmtEpEltInqNext</b> function returns one element from an endpoint map.


## -parameters




### -param InquiryContext

Specifies an inquiry context. The inquiry context is returned from 
<a href="https://msdn.microsoft.com/659ab657-e17f-46a9-942e-aa2631c1716d">RpcMgmtEpEltInqBegin</a>.


### -param IfId

Returns the interface identifier of the endpoint-map element.


### -param Binding

Optional. Returns the binding handle from the endpoint-map element.


#### - ObjectUuid

Optional. Returns the object UUID from the endpoint-map element.


### -param Annotation

Optional. Returns the annotation string for the endpoint-map element. When there is no annotation string in the endpoint-map element, the empty string ("") is returned.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcMgmtEpEltInqNext</b> function returns one element from the endpoint map. Elements selected depend on the inquiry context. The selection criteria are determined by <i>InquiryType</i> of the 
<a href="https://msdn.microsoft.com/659ab657-e17f-46a9-942e-aa2631c1716d">RpcMgmtEpEltInqBegin</a> function that returned <i>InquiryContext</i>.

An application can view all the selected endpoint-map elements by repeatedly calling 
<b>RpcMgmtEpEltInqNext</b>. When all the elements have been viewed, this function returns an RPC_X_NO_MORE_ENTRIES status. The returned elements are unordered.

When the respective arguments are non-NULL, the RPC run-time function library allocates memory for <i>Binding</i> and <i>Annotation</i> on each call to this function. The application is responsible for calling 
<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a> for each returned <i>Binding</i> and 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> for each returned <i>Annotation</i>.

After viewing the endpoint-map elements, the application must call 
<a href="https://msdn.microsoft.com/7a0aac99-8829-4720-a388-da88d015d596">RpcMgmtEpEltInqDone</a> to delete the inquiry context.




## -see-also




<a href="https://msdn.microsoft.com/35656cdd-b1ae-43d3-a5c7-92bdb7726d5b">RpcEpRegister</a>



<a href="https://msdn.microsoft.com/659ab657-e17f-46a9-942e-aa2631c1716d">RpcMgmtEpEltInqBegin</a>



<a href="https://msdn.microsoft.com/7a0aac99-8829-4720-a388-da88d015d596">RpcMgmtEpEltInqDone</a>
 

 

