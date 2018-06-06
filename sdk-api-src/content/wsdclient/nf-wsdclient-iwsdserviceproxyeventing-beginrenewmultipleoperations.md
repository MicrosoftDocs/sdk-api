---
UID: NF:wsdclient.IWSDServiceProxyEventing.BeginRenewMultipleOperations
title: IWSDServiceProxyEventing::BeginRenewMultipleOperations
author: windows-sdk-content
description: Initializes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.
old-location: ncd\iwsdserviceproxyeventing_beginrenewmultipleoperations.htm
old-project: WsdApi
ms.assetid: ac93a29a-789f-4aa0-b804-b4d0a5b89ee2
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: BeginRenewMultipleOperations, BeginRenewMultipleOperations method, BeginRenewMultipleOperations method,IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,BeginRenewMultipleOperations method, IWSDServiceProxyEventing.BeginRenewMultipleOperations, IWSDServiceProxyEventing::BeginRenewMultipleOperations, ncd.iwsdserviceproxyeventing_beginrenewmultipleoperations, wsdclient/IWSDServiceProxyEventing::BeginRenewMultipleOperations
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
 - IWSDServiceProxyEventing.BeginRenewMultipleOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDServiceProxyEventing::BeginRenewMultipleOperations


## -description


Initializes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.


## -parameters




### -param pOperations [in]

Pointer to an array of references to <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structures that specify the operation subscriptions to renew.


### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.


### -param pExpires [in]

Pointer to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specifies requested duration for the subscription.


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
 

 

