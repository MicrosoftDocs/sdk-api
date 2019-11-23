---
UID: NN:wsdclient.IWSDAsyncResult
title: IWSDAsyncResult (wsdclient.h)

description: Represents an asynchronous operation.
old-location: ncd\iwsdasyncresult.htm
tech.root: WsdApi
ms.assetid: 49c5ad02-f24b-4ef9-b943-483728c0bbcd

ms.date: 12/05/2018
ms.keywords: IWSDAsyncResult, IWSDAsyncResult interface, IWSDAsyncResult interface,described, ncd.iwsdasyncresult, wsdclient/IWSDAsyncResult
ms.topic: interface
f1_keywords:
- wsdclient/IWSDAsyncResult
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDAsyncResult interface


## -description


Represents an asynchronous operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDAsyncResult</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDAsyncResult</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasyncresult-abort">Abort</a>
</td>
<td align="left" width="63%">
Aborts the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasyncresult-getasyncstate">GetAsyncState</a>
</td>
<td align="left" width="63%">
Gets the state of the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasyncresult-getendpointproxy">GetEndpointProxy</a>
</td>
<td align="left" width="63%">
Retrieves the endpoint proxy for the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasyncresult-getevent">GetEvent</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_event">WSD_EVENT</a> structure that contains the result of the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasyncresult-hascompleted">HasCompleted</a>
</td>
<td align="left" width="63%">
Indicates whether the operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasyncresult-setcallback">SetCallback</a>
</td>
<td align="left" width="63%">
Specifies a callback interface to call when the asynchronous operation has completed. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasyncresult-setwaithandle">SetWaitHandle</a>
</td>
<td align="left" width="63%">
Specifies a wait handle to set when the operation completes.

</td>
</tr>
</table> 


## -remarks



The <b>IWSDAsyncResult</b> interface can be used to set a wait handle to receive event or message notification or poll for operation completion. It can also retrieve the state of an asynchronous operation and retrieve the results and response body of the event.

The <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasynccallback">IWSDAsyncCallback</a> interface can be used to provide an asynchronous calling pattern in support of WSDAPI messaging and eventing, allowing an application to receive callback notification based on the status of an operation.



A failed asynchronous operation is treated as a completed asynchronous operation. Error or fault information can be retrieved from the <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasynccallback">IWSDAsyncCallback</a> interface using the <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasynccallback-asyncoperationcomplete">IWSDAsyncCallback::AsyncOperationComplete</a> method.



