---
UID: NF:wsdclient.IWSDServiceProxyEventing.EndRenewMultipleOperations
title: IWSDServiceProxyEventing::EndRenewMultipleOperations
author: windows-sdk-content
description: Completes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.
old-location: ncd\iwsdserviceproxyeventing_endrenewmultipleoperations.htm
tech.root: wsdapi
ms.assetid: fb5be204-a775-4abb-af5b-9a829b69fa14
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EndRenewMultipleOperations, EndRenewMultipleOperations method, EndRenewMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,EndRenewMultipleOperations method, IWSDServiceProxyEventing.EndRenewMultipleOperations, IWSDServiceProxyEventing::EndRenewMultipleOperations, ncd.iwsdserviceproxyeventing_endrenewmultipleoperations, wsdclient/IWSDServiceProxyEventing::EndRenewMultipleOperations
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
 - IWSDServiceProxyEventing.EndRenewMultipleOperations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDServiceProxyEventing::EndRenewMultipleOperations


## -description


Completes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.


## -parameters




### -param pOperations [in]

Pointer to an array of references to <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structures that specify the operation subscriptions to renew.


### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.


### -param pResult [in]

Pointer to an <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> interface that represents the result of the requests upon completion.


### -param ppExpires [out]

Pointer to a pointer to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specfies the duration of the subscription that was just renewed.  Upon completion, call  <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a> to free the memory.  This parameter is optional. 


### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of event subscriptions. When done, call  <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a>.  This parameter is optional.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c9454636-6d6a-4344-a954-1bd35195aff9">IWSDServiceProxyEventing</a>
 

 

