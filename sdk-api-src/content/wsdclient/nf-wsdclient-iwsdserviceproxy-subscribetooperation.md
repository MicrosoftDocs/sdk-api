---
UID: NF:wsdclient.IWSDServiceProxy.SubscribeToOperation
title: IWSDServiceProxy::SubscribeToOperation
author: windows-sdk-content
description: Subscribes to a notification or solicit/response event.
old-location: ncd\iwsdserviceproxy_subscribetooperation_method.htm
old-project: WsdApi
ms.assetid: d3294bd7-f3df-4571-92f6-eb6bc57240fb
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWSDServiceProxy interface,SubscribeToOperation method, IWSDServiceProxy.SubscribeToOperation, IWSDServiceProxy::SubscribeToOperation, SubscribeToOperation, SubscribeToOperation method, SubscribeToOperation method,IWSDServiceProxy interface, ncd.iwsdserviceproxy_subscribetooperation_method, wsdclient/IWSDServiceProxy::SubscribeToOperation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDServiceProxy.SubscribeToOperation
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDServiceProxy::SubscribeToOperation


## -description


Subscribes to a notification or solicit/response event.


## -parameters




### -param pOperation [in]

 Reference to a <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structure that specifies the operation to subscribe to. 



### -param pUnknown [in]

 
Anonymous data passed to a client eventing callback function. This data is used to associate a client object with the subscription.


### -param pAny [in]

Extensible data to be added to the body of the subscription request. You can use the IWSDXML* interfaces to build the data. For details, see <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a>.


### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of event subscriptions. When done, call  <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a>. Do not release this object.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The proxy has already subscribed to the operation specified by <i>pOperation</i>.

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
 




## -remarks



This method is normally only called by generated proxy code.




## -see-also




<a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a>
 

 

