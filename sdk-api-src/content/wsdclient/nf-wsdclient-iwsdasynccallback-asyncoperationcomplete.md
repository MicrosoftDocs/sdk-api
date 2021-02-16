---
UID: NF:wsdclient.IWSDAsyncCallback.AsyncOperationComplete
title: IWSDAsyncCallback::AsyncOperationComplete (wsdclient.h)
description: Indicates that the asynchronous operation has completed.
helpviewer_keywords: ["AsyncOperationComplete","AsyncOperationComplete method","AsyncOperationComplete method","IWSDAsyncCallback interface","IWSDAsyncCallback interface","AsyncOperationComplete method","IWSDAsyncCallback.AsyncOperationComplete","IWSDAsyncCallback::AsyncOperationComplete","ncd.iwsdasynccallback_asyncoperationcomplete_method","wsdclient/IWSDAsyncCallback::AsyncOperationComplete"]
old-location: ncd\iwsdasynccallback_asyncoperationcomplete_method.htm
tech.root: ncd
ms.assetid: f2272d1e-bb12-43cd-a0ae-80530ad25fcf
ms.date: 12/05/2018
ms.keywords: AsyncOperationComplete, AsyncOperationComplete method, AsyncOperationComplete method,IWSDAsyncCallback interface, IWSDAsyncCallback interface,AsyncOperationComplete method, IWSDAsyncCallback.AsyncOperationComplete, IWSDAsyncCallback::AsyncOperationComplete, ncd.iwsdasynccallback_asyncoperationcomplete_method, wsdclient/IWSDAsyncCallback::AsyncOperationComplete
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
 - IWSDAsyncCallback::AsyncOperationComplete
 - wsdclient/IWSDAsyncCallback::AsyncOperationComplete
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
 - IWSDAsyncCallback.AsyncOperationComplete
---

# IWSDAsyncCallback::AsyncOperationComplete


## -description

Indicates that the asynchronous operation has completed.

## -parameters

### -param pAsyncResult [in]

Pointer to an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> object that contains the user-defined state information passed to <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasyncresult-setcallback">IWSDAsyncResult::SetCallback</a>.

### -param pAsyncState [in]

The state of the asynchronous operation.

## -returns

Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
</table>

## -remarks

The value returned by <b>AsyncOperationComplete</b> is ignored.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasynccallback">IWSDAsyncCallback</a>