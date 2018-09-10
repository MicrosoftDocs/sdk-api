---
UID: NN:wsdclient.IWSDAsyncCallback
title: IWSDAsyncCallback
author: windows-sdk-content
description: Handles callbacks for the completion of an asynchronous operation.
old-location: ncd\iwsdasynccallback.htm
tech.root: WsdApi
ms.assetid: 24108143-55b7-4098-a4cc-025dfdfd054a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSDAsyncCallback, IWSDAsyncCallback interface, IWSDAsyncCallback interface,described, ncd.iwsdasynccallback, wsdclient/IWSDAsyncCallback
ms.prod: windows
ms.technology: windows-sdk
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
 - IWSDAsyncCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDAsyncCallback interface


## -description


Handles callbacks for the completion of an asynchronous operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDAsyncCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDAsyncCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDAsyncCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2272d1e-bb12-43cd-a0ae-80530ad25fcf">AsyncOperationComplete</a>
</td>
<td align="left" width="63%">
Indicates that the asynchronous operation has completed.

</td>
</tr>
</table> 


## -remarks



This interface provides an asynchronous calling pattern in support of WSDAPI messaging and eventing, allowing an application to receive callback notification based on the status of an operation.

The <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> interface can be used to wait for event notification or to poll for operation completion if asynchronous callbacks are not required.



