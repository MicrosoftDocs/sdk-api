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

# IWSDEndpointProxy::SendTwoWayRequest


## -description


Sends a two-way request message using a synchronous call pattern.


## -parameters




### -param pBody [in]

The body of the message.


### -param pOperation [in]

Reference to a <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structure that specifies the operation to perform.


### -param pResponseContext [in, optional]

 Reference to a <a href="https://msdn.microsoft.com/591cf076-f55f-4e78-aa5e-94ea8db3d102">WSD_SYNCHRONOUS_RESPONSE_CONTEXT</a> structure or other context structure that specifies the context for handling the response to the request. 



## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pOperation</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method is normally only called by generated proxy code.




<a href="https://msdn.microsoft.com/591cf076-f55f-4e78-aa5e-94ea8db3d102">WSD_SYNCHRONOUS_RESPONSE_CONTEXT</a> is used for the <i>responseContext</i> value when a synchronous call pattern is used. 




## -see-also




<a href="https://msdn.microsoft.com/58ca085f-8939-413c-8fd3-4d867b1cf490">IWSDEndpointProxy</a>
 

 

