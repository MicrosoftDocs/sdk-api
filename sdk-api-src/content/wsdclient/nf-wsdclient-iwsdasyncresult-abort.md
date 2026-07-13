---
UID: NF:wsdclient.IWSDAsyncResult.Abort
title: IWSDAsyncResult::Abort (wsdclient.h)
description: Aborts the asynchronous operation.
helpviewer_keywords: ["Abort","Abort method","Abort method","IWSDAsyncResult interface","IWSDAsyncResult interface","Abort method","IWSDAsyncResult.Abort","IWSDAsyncResult::Abort","ncd.iwsdasyncresult_abort","wsdclient/IWSDAsyncResult::Abort"]
old-location: ncd\iwsdasyncresult_abort.htm
tech.root: ncd
ms.assetid: 9237bcb4-4404-4d15-a18a-1d651e3fb899
ms.date: 12/05/2018
ms.keywords: Abort, Abort method, Abort method,IWSDAsyncResult interface, IWSDAsyncResult interface,Abort method, IWSDAsyncResult.Abort, IWSDAsyncResult::Abort, ncd.iwsdasyncresult_abort, wsdclient/IWSDAsyncResult::Abort
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
 - IWSDAsyncResult::Abort
 - wsdclient/IWSDAsyncResult::Abort
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
 - IWSDAsyncResult.Abort
---

# IWSDAsyncResult::Abort


## -description

Aborts the asynchronous operation.



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
Method completed successfully.

</td>
</tr>
</table>

## -remarks

<b>Abort</b> waits for all pending callbacks set with <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasyncresult-setcallback">SetCallback</a> to complete before returning to the caller.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a>
