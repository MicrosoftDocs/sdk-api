---
UID: NN:wsdclient.IWSDAsyncResult
title: IWSDAsyncResult (wsdclient.h)
author: windows-sdk-content
description: Represents an asynchronous operation.
old-location: ncd\iwsdasyncresult.htm
tech.root: WsdApi
ms.assetid: 49c5ad02-f24b-4ef9-b943-483728c0bbcd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDAsyncResult, IWSDAsyncResult interface, IWSDAsyncResult interface,described, ncd.iwsdasyncresult, wsdclient/IWSDAsyncResult
ms.topic: interface
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
 - IWSDAsyncResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDAsyncResult interface


## -description


Represents an asynchronous operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDAsyncResult</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDAsyncResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDAsyncResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9237bcb4-4404-4d15-a18a-1d651e3fb899">Abort</a>
</td>
<td align="left" width="63%">
Aborts the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f4115bd-748e-41cd-928f-3dd3a354d336">GetAsyncState</a>
</td>
<td align="left" width="63%">
Gets the state of the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2b1f43a-e86c-4ec9-a39f-9c5050f3e3c3">GetEndpointProxy</a>
</td>
<td align="left" width="63%">
Retrieves the endpoint proxy for the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de201c8b-9052-42f9-b95d-3b65cf0c86a3">GetEvent</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://msdn.microsoft.com/d8697474-bfe5-4704-b1ac-15cf96f2ca92">WSD_EVENT</a> structure that contains the result of the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67944519-c6cc-4dc8-9035-4e6ee84e1277">HasCompleted</a>
</td>
<td align="left" width="63%">
Indicates whether the operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39fc05f8-4b09-4305-b9a4-b4ef65788efc">SetCallback</a>
</td>
<td align="left" width="63%">
Specifies a callback interface to call when the asynchronous operation has completed. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7196785-0e9c-4320-a14e-60457f72c66b">SetWaitHandle</a>
</td>
<td align="left" width="63%">
Specifies a wait handle to set when the operation completes.

</td>
</tr>
</table> 


## -remarks



The <b>IWSDAsyncResult</b> interface can be used to set a wait handle to receive event or message notification or poll for operation completion. It can also retrieve the state of an asynchronous operation and retrieve the results and response body of the event.

The <a href="https://msdn.microsoft.com/24108143-55b7-4098-a4cc-025dfdfd054a">IWSDAsyncCallback</a> interface can be used to provide an asynchronous calling pattern in support of WSDAPI messaging and eventing, allowing an application to receive callback notification based on the status of an operation.



A failed asynchronous operation is treated as a completed asynchronous operation. Error or fault information can be retrieved from the <a href="https://msdn.microsoft.com/24108143-55b7-4098-a4cc-025dfdfd054a">IWSDAsyncCallback</a> interface using the <a href="https://msdn.microsoft.com/f2272d1e-bb12-43cd-a0ae-80530ad25fcf">IWSDAsyncCallback::AsyncOperationComplete</a> method.



