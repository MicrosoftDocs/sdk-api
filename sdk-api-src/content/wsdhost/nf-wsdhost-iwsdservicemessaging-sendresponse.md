---
UID: NF:wsdhost.IWSDServiceMessaging.SendResponse
title: IWSDServiceMessaging::SendResponse
author: windows-sdk-content
description: Sends a response message matching a given request context.
old-location: ncd\iwsdservicemessaging_sendresponse.htm
tech.root: wsdapi
ms.assetid: ec136c44-b8f5-42db-a965-2dd5b3cd18ad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSDServiceMessaging interface,SendResponse method, IWSDServiceMessaging.SendResponse, IWSDServiceMessaging::SendResponse, SendResponse, SendResponse method, SendResponse method,IWSDServiceMessaging interface, ncd.iwsdservicemessaging_sendresponse, wsdhost/IWSDServiceMessaging::SendResponse
ms.topic: method
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdhost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDServiceMessaging.SendResponse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDServiceMessaging::SendResponse


## -description


Sends a response message matching a given request context. This method should be called only from <a href="https://msdn.microsoft.com/76dffca8-bb84-4384-a9e8-120a4cf2acac">generated code</a>.


## -parameters




### -param pBody [in]

Pointer to the message body to send in the response message.


### -param pOperation [in]

Pointer to a <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structure that contains the type of response to send.


### -param pMessageParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a> object that contains the message parameters from the original request message.


## -returns



Possible return values include, but are not limited to, the following.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pOperation</i> or <i>pMessageParameters</i> is <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The method could not be completed.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/06584474-1c55-43db-9c7a-fefea8d16eed">IWSDServiceMessaging</a>
 

 

