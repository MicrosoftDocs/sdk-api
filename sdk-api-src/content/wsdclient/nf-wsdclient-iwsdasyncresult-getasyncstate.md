---
UID: NF:wsdclient.IWSDAsyncResult.GetAsyncState
title: IWSDAsyncResult::GetAsyncState (wsdclient.h)
description: Gets the state of the asynchronous operation.
helpviewer_keywords: ["GetAsyncState","GetAsyncState method","GetAsyncState method","IWSDAsyncResult interface","IWSDAsyncResult interface","GetAsyncState method","IWSDAsyncResult.GetAsyncState","IWSDAsyncResult::GetAsyncState","ncd.iwsdasyncresult_getasyncstate_method","wsdclient/IWSDAsyncResult::GetAsyncState"]
old-location: ncd\iwsdasyncresult_getasyncstate_method.htm
tech.root: ncd
ms.assetid: 4f4115bd-748e-41cd-928f-3dd3a354d336
ms.date: 12/05/2018
ms.keywords: GetAsyncState, GetAsyncState method, GetAsyncState method,IWSDAsyncResult interface, IWSDAsyncResult interface,GetAsyncState method, IWSDAsyncResult.GetAsyncState, IWSDAsyncResult::GetAsyncState, ncd.iwsdasyncresult_getasyncstate_method, wsdclient/IWSDAsyncResult::GetAsyncState
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
 - IWSDAsyncResult::GetAsyncState
 - wsdclient/IWSDAsyncResult::GetAsyncState
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
 - IWSDAsyncResult.GetAsyncState
---

# IWSDAsyncResult::GetAsyncState


## -description

Gets the state of the asynchronous operation.

## -parameters

### -param ppAsyncState [out]

User-defined state information.

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
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAsyncState</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a>