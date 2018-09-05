---
UID: NF:wsdclient.IWSDServiceProxyEventing.SubscribeToMultipleOperations
title: IWSDServiceProxyEventing::SubscribeToMultipleOperations
author: windows-sdk-content
description: Subscribes to a collection of notifications or solicit/response events.
old-location: ncd\iwsdserviceproxyeventing_subscribetomultipleoperations.htm
old-project: WsdApi
ms.assetid: 0df5b429-5b6e-4cef-af05-7f615c93aa0f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSDServiceProxyEventing interface,SubscribeToMultipleOperations method, IWSDServiceProxyEventing.SubscribeToMultipleOperations, IWSDServiceProxyEventing::SubscribeToMultipleOperations, SubscribeToMultipleOperations, SubscribeToMultipleOperations method, SubscribeToMultipleOperations method,IWSDServiceProxyEventing interface, ncd.iwsdserviceproxyeventing_subscribetomultipleoperations, wsdclient/IWSDServiceProxyEventing::SubscribeToMultipleOperations
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdclient.idl
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
 - wsdapi.dll
api_name:
 - IWSDServiceProxyEventing.SubscribeToMultipleOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDServiceProxyEventing::SubscribeToMultipleOperations


## -description


Subscribes to a collection of notifications or solicit/response events.


## -parameters




### -param pOperations [in]

Pointer to an array of references to <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structures that specify the operations of whcih to subscribe. 



### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.


### -param pUnknown [in]

Anonymous data passed to a client eventing callback function. This data is used to associate a client object with the subscription.


### -param pExpires [in]

Pointer to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specifies requested duration for the subscription.


### -param pAny [in]

Pointer to extensible data to be added to the body of the request.  This parameter is optional.


### -param ppExpires [out]

Pointer to a pointer to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specfies the duration of the subscription.  Upon completion, call  <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a> to free the memory.   This parameter is optional.


### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of event subscriptions. When done, call  <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a>.   This parameter is optional.


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



This method is designed to be exclusively called by generated proxy code.

The method is synchronous and will return when the requests have completed or the expiration criteria have been satisfied.




## -see-also




<a href="https://msdn.microsoft.com/c9454636-6d6a-4344-a954-1bd35195aff9">IWSDServiceProxyEventing</a>
 

 

