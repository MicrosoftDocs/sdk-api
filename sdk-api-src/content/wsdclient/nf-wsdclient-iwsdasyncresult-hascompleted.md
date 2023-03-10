---
UID: NF:wsdclient.IWSDAsyncResult.HasCompleted
title: IWSDAsyncResult::HasCompleted (wsdclient.h)
description: Indicates whether the operation has completed.
helpviewer_keywords: ["HasCompleted","HasCompleted method","HasCompleted method","IWSDAsyncResult interface","IWSDAsyncResult interface","HasCompleted method","IWSDAsyncResult.HasCompleted","IWSDAsyncResult::HasCompleted","ncd.iwsdasyncresult_hascompleted_method","wsdclient/IWSDAsyncResult::HasCompleted"]
old-location: ncd\iwsdasyncresult_hascompleted_method.htm
tech.root: ncd
ms.assetid: 67944519-c6cc-4dc8-9035-4e6ee84e1277
ms.date: 12/05/2018
ms.keywords: HasCompleted, HasCompleted method, HasCompleted method,IWSDAsyncResult interface, IWSDAsyncResult interface,HasCompleted method, IWSDAsyncResult.HasCompleted, IWSDAsyncResult::HasCompleted, ncd.iwsdasyncresult_hascompleted_method, wsdclient/IWSDAsyncResult::HasCompleted
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDAsyncResult::HasCompleted
 - wsdclient/IWSDAsyncResult::HasCompleted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDAsyncResult.HasCompleted
---

# IWSDAsyncResult::HasCompleted


## -description

Indicates whether the operation has completed.



## -returns

This method can return one of these values.


Possible return values include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The operation has not completed.

</td>
</tr>
</table>

## -remarks

A failed asynchronous operation is treated as a completed asynchronous operation. Error or fault information can be retrieved from the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasynccallback">IWSDAsyncCallback</a> interface using the <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasynccallback-asyncoperationcomplete">IWSDAsyncCallback::AsyncOperationComplete</a> method.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a>
