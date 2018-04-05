---
UID: NF:wsdclient.IWSDServiceProxyEventing.EndUnsubscribeToMultipleOperations
title: IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations method
author: windows-driver-content
description: Completes an asynchronous cancellation request for a subscription to a collection of notifications or solicit/response events.
old-location: ncd\iwsdserviceproxyeventing_endunsubscribetomultipleoperations.htm
old-project: WsdApi
ms.assetid: 62f42441-11b0-46ce-9a4e-03b34d8b4c9b
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: EndUnsubscribeToMultipleOperations method, EndUnsubscribeToMultipleOperations method, IWSDServiceProxyEventing interface, EndUnsubscribeToMultipleOperations,IWSDServiceProxyEventing.EndUnsubscribeToMultipleOperations, IWSDServiceProxyEventing, IWSDServiceProxyEventing interface, EndUnsubscribeToMultipleOperations method, IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations, ncd.iwsdserviceproxyeventing_endunsubscribetomultipleoperations, wsdclient/IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wsdapi.dll
api_name:
-	IWSDServiceProxyEventing.EndUnsubscribeToMultipleOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDServiceProxyEventing::EndUnsubscribeToMultipleOperations method


## -description


Completes an  asynchronous cancellation request for a subscription to  a collection of notifications or solicit/response events.


## -parameters




### -param pOperations [in]

Pointer to an array of references to <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structures that specifies the operations from which to unsubscribe. 



### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.


### -param pResult [out]

Pointer to an <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> interface that will represent the result of the requests upon completion.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c9454636-6d6a-4344-a954-1bd35195aff9">IWSDServiceProxyEventing</a>
 

 

