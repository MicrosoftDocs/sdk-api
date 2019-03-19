---
UID: NF:wsdclient.IWSDServiceProxyEventing.BeginSubscribeToMultipleOperations
title: IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations (wsdclient.h)
author: windows-sdk-content
description: Initializes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.
old-location: ncd\iwsdserviceproxyeventing_beginsubscribetomultipleoperations.htm
tech.root: WsdApi
ms.assetid: 54c6ac58-4272-45ad-80cc-2114ba6f466e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BeginSubscribeToMultipleOperations, BeginSubscribeToMultipleOperations method, BeginSubscribeToMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,BeginSubscribeToMultipleOperations method, IWSDServiceProxyEventing.BeginSubscribeToMultipleOperations, IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations, ncd.iwsdserviceproxyeventing_beginsubscribetomultipleoperations, wsdclient/IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations
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
 - IWSDServiceProxyEventing.BeginSubscribeToMultipleOperations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDServiceProxyEventing::BeginSubscribeToMultipleOperations


## -description


Initializes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.


## -parameters




### -param pOperations [in]

Pointer to an array of references to <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structures that specify the operations of which to subscribe.


### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.


### -param pUnknown [in]

Anonymous data passed to a client eventing callback function. This data is used to associate a client object with the subscription.


### -param pExpires [in]

Pointer to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specifies the requested duration for the subscription.


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




## -remarks



This method is designed to be exclusively called by generated proxy code.

The method is asynchronous and will return immediately.    The caller should subsequently call <a href="https://msdn.microsoft.com/2e3cdb10-fde9-4936-9a7d-61404a754faa">EndSubscribeToMultipleOperations</a>.




## -see-also




<a href="https://msdn.microsoft.com/c9454636-6d6a-4344-a954-1bd35195aff9">IWSDServiceProxyEventing</a>
 

 

