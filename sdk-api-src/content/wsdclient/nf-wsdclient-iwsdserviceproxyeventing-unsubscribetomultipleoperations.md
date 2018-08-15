---
UID: NF:wsdclient.IWSDServiceProxyEventing.UnsubscribeToMultipleOperations
title: IWSDServiceProxyEventing::UnsubscribeToMultipleOperations
author: windows-sdk-content
description: Cancels a collection of subscriptions to notifications or solicit/response events.
old-location: ncd\iwsdserviceproxyeventing_unsubscribetomultipleoperations.htm
old-project: wsdapi
ms.assetid: 2f542dc1-639c-4201-9274-8aa5cc238482
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWSDServiceProxyEventing interface,UnsubscribeToMultipleOperations method, IWSDServiceProxyEventing.UnsubscribeToMultipleOperations, IWSDServiceProxyEventing::UnsubscribeToMultipleOperations, UnsubscribeToMultipleOperations, UnsubscribeToMultipleOperations method, UnsubscribeToMultipleOperations method,IWSDServiceProxyEventing interface, ncd.iwsdserviceproxyeventing_unsubscribetomultipleoperations, wsdclient/IWSDServiceProxyEventing::UnsubscribeToMultipleOperations
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
 - IWSDServiceProxyEventing.UnsubscribeToMultipleOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDServiceProxyEventing::UnsubscribeToMultipleOperations


## -description


Cancels a collection of subscriptions to notifications or solicit/response events.


## -parameters




### -param pOperations [in]

Pointer to an array of references to <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structures that specify the operations to unsubscribe from. 



### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.


### -param pAny [in]

Pointer to extensible data to be added to the body of the request.


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
The proxy is not subscribed to the notification specified by <i>pOperation</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pOperation</i> is NULL.

</td>
</tr>
</table>
 




## -remarks



This method is designed to be exclusively called by generated proxy code.




## -see-also




<a href="https://msdn.microsoft.com/c9454636-6d6a-4344-a954-1bd35195aff9">IWSDServiceProxyEventing</a>
 

 

