---
UID: NF:wsdclient.IWSDServiceProxyEventing.RenewMultipleOperations
title: IWSDServiceProxyEventing::RenewMultipleOperations
author: windows-sdk-content
description: Renews a collection of existing notification subscriptions by submitting a new duration.
old-location: ncd\iwsdserviceproxyeventing_renewmultipleoperations.htm
tech.root: WsdApi
ms.assetid: 67c5fa63-3512-4b03-afb4-9b97b26200aa
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWSDServiceProxyEventing interface,RenewMultipleOperations method, IWSDServiceProxyEventing.RenewMultipleOperations, IWSDServiceProxyEventing::RenewMultipleOperations, RenewMultipleOperations, RenewMultipleOperations method, RenewMultipleOperations method,IWSDServiceProxyEventing interface, ncd.iwsdserviceproxyeventing_renewmultipleoperations, wsdclient/IWSDServiceProxyEventing::RenewMultipleOperations
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDServiceProxyEventing.RenewMultipleOperations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wsdclient.h
: 
- IWSDServiceProxyEventing.RenewMultipleOperations
: 
---

# IWSDServiceProxyEventing::RenewMultipleOperations


## -description


Renews a collection of existing notification subscriptions by submitting a new duration.


## -parameters




### -param pOperations [in]

Pointer to an array of references to <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structures that specify the operation subscriptions to renew.


### -param dwOperationCount [in]

The number of elements in the array in <i>pOperations</i>.


### -param pExpires [in]

Pointer to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specifies requested duration for the subscription.


### -param pAny [in]

Pointer to extensible data to be added to the body of the request.  This parameter is optional.


### -param ppExpires [out]

Pointer to a pointer to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specifies the duration of the subscription that was just renewed.  Upon completion, call  <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a> to free the memory.  This parameter is optional.


### -param ppAny [out]

Extensible data that the remote device can add to the subscription response. This allows services to provide additional customization of renew requests. When done, call  <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a> to free the memory. For details, see <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a>.  This parameter is optional.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c9454636-6d6a-4344-a954-1bd35195aff9">IWSDServiceProxyEventing</a>
 

 

