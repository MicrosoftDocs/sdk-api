---
UID: NF:wsdclient.IWSDServiceProxyEventing.EndSubscribeToMultipleOperations
title: IWSDServiceProxyEventing::EndSubscribeToMultipleOperations
author: windows-sdk-content
description: Completes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.
old-location: ncd\iwsdserviceproxyeventing_endsubscribetomultipleoperations.htm
old-project: WsdApi
ms.assetid: 2e3cdb10-fde9-4936-9a7d-61404a754faa
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: EndSubscribeToMultipleOperations, EndSubscribeToMultipleOperations method, EndSubscribeToMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,EndSubscribeToMultipleOperations method, IWSDServiceProxyEventing.EndSubscribeToMultipleOperations, IWSDServiceProxyEventing::EndSubscribeToMultipleOperations, ncd.iwsdserviceproxyeventing_endsubscribetomultipleoperations, wsdclient/IWSDServiceProxyEventing::EndSubscribeToMultipleOperations
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
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
 - IWSDServiceProxyEventing.EndSubscribeToMultipleOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDServiceProxyEventing::EndSubscribeToMultipleOperations


## -description


Completes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.


## -parameters




### -param pOperations [in]

Pointer to an array of references to <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structures that specify the subscribed operations. 



### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.


### -param pResult [out]

Pointer to an <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> interface that represents the result of the requests upon completion.


### -param ppExpires [out]

Pointer to a pointer to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specfies the duration of the subscription.  Upon completion, call  <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a> to free the memory.  This parameter is optional. 


### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of event subscriptions. When done, call  <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a>.  This parameter is optional.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is designed to be exclusively called by generated proxy code.

The method is used to obtain the results from a previous asynchronous <a href="https://msdn.microsoft.com/54c6ac58-4272-45ad-80cc-2114ba6f466e">BeginSubscribeToMultipleOperations</a> call.




## -see-also




<a href="https://msdn.microsoft.com/c9454636-6d6a-4344-a954-1bd35195aff9">IWSDServiceProxyEventing</a>
 

 

