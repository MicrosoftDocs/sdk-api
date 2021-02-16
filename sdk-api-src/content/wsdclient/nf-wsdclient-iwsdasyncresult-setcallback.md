---
UID: NF:wsdclient.IWSDAsyncResult.SetCallback
title: IWSDAsyncResult::SetCallback (wsdclient.h)
description: Specifies a callback interface to call when the asynchronous operation has completed.
helpviewer_keywords: ["IWSDAsyncResult interface","SetCallback method","IWSDAsyncResult.SetCallback","IWSDAsyncResult::SetCallback","SetCallback","SetCallback method","SetCallback method","IWSDAsyncResult interface","ncd.iwsdasyncresult_setcallback","wsdclient/IWSDAsyncResult::SetCallback"]
old-location: ncd\iwsdasyncresult_setcallback.htm
tech.root: ncd
ms.assetid: 39fc05f8-4b09-4305-b9a4-b4ef65788efc
ms.date: 12/05/2018
ms.keywords: IWSDAsyncResult interface,SetCallback method, IWSDAsyncResult.SetCallback, IWSDAsyncResult::SetCallback, SetCallback, SetCallback method, SetCallback method,IWSDAsyncResult interface, ncd.iwsdasyncresult_setcallback, wsdclient/IWSDAsyncResult::SetCallback
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDAsyncResult::SetCallback
 - wsdclient/IWSDAsyncResult::SetCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDAsyncResult.SetCallback
---

# IWSDAsyncResult::SetCallback


## -description

Specifies a callback interface to call when the asynchronous operation has completed.

## -parameters

### -param pCallback [in]

Pointer to a <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasynccallback">IWSDAsyncCallback</a> object that contains the callback implemented by the user.

### -param pAsyncState [in]

User-defined state information to pass to the callback.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pCallback</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsdasynccallback-asyncoperationcomplete">IWSDAsyncCallback::AsyncOperationComplete</a> method is passed the result object associated with the completing message and the state. 

<i>pCallback</i> is released when the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> object is destroyed.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a>