---
UID: NF:wsdclient.IWSDServiceProxyEventing.BeginUnsubscribeToMultipleOperations
title: IWSDServiceProxyEventing::BeginUnsubscribeToMultipleOperations
author: windows-sdk-content
description: Initializes an asynchronous cancelation request for a subscription to a collection of notifications or solicit/response events.
old-location: ncd\iwsdserviceproxyeventing_beginunsubscribetomultipleoperations.htm
tech.root: WsdApi
ms.assetid: a8a3dd48-89a2-4d7b-98e0-3dcb3c32cb2b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BeginUnsubscribeToMultipleOperations, BeginUnsubscribeToMultipleOperations method, BeginUnsubscribeToMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,BeginUnsubscribeToMultipleOperations method, IWSDServiceProxyEventing.BeginUnsubscribeToMultipleOperations, IWSDServiceProxyEventing::BeginUnsubscribeToMultipleOperations, ncd.iwsdserviceproxyeventing_beginunsubscribetomultipleoperations, wsdclient/IWSDServiceProxyEventing::BeginUnsubscribeToMultipleOperations
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
 - IWSDServiceProxyEventing.BeginUnsubscribeToMultipleOperations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDServiceProxyEventing::BeginUnsubscribeToMultipleOperations


## -description


Initializes an  asynchronous cancelation request for a subscription to  a collection of notifications or solicit/response events.


## -parameters




### -param pOperations [in]

Pointer to an array of references to <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structures that specify the operations to unsubscribe from. 



### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.


### -param pAny [in]

Pointer to extensible data to be added to the body of the request.  This parameter is optional.


### -param pAsyncState [in]

Anonymous data passed to <i>pAsyncCallback</i> when the callback is called.  This data is used to associate a client object with the pending operation.  This parameter is optional.


### -param pAsyncCallback [in]

Reference to an <a href="https://msdn.microsoft.com/24108143-55b7-4098-a4cc-025dfdfd054a">IWSDAsyncCallback</a> object that performs the message callback status notifications.  This parameter is optional.


### -param ppResult [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> interface that will represent the result of the requests upon completion.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c9454636-6d6a-4344-a954-1bd35195aff9">IWSDServiceProxyEventing</a>
 

 

