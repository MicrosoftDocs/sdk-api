---
UID: NF:wsdclient.IWSDAsyncResult.SetWaitHandle
title: IWSDAsyncResult::SetWaitHandle (wsdclient.h)
description: Specifies a wait handle to set when the operation completes.
helpviewer_keywords: ["IWSDAsyncResult interface","SetWaitHandle method","IWSDAsyncResult.SetWaitHandle","IWSDAsyncResult::SetWaitHandle","SetWaitHandle","SetWaitHandle method","SetWaitHandle method","IWSDAsyncResult interface","ncd.iwsdasyncresult_setwaithandle_method","wsdclient/IWSDAsyncResult::SetWaitHandle"]
old-location: ncd\iwsdasyncresult_setwaithandle_method.htm
tech.root: ncd
ms.assetid: d7196785-0e9c-4320-a14e-60457f72c66b
ms.date: 12/05/2018
ms.keywords: IWSDAsyncResult interface,SetWaitHandle method, IWSDAsyncResult.SetWaitHandle, IWSDAsyncResult::SetWaitHandle, SetWaitHandle, SetWaitHandle method, SetWaitHandle method,IWSDAsyncResult interface, ncd.iwsdasyncresult_setwaithandle_method, wsdclient/IWSDAsyncResult::SetWaitHandle
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
 - IWSDAsyncResult::SetWaitHandle
 - wsdclient/IWSDAsyncResult::SetWaitHandle
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
 - IWSDAsyncResult.SetWaitHandle
---

# IWSDAsyncResult::SetWaitHandle


## -description

Specifies a wait handle to set when the operation completes.

## -parameters

### -param hWaitHandle [in]

The wait handle to set.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>hWaitHandle</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>

## -remarks

Do not close <i>hWaitHandle</i> until after the asynchronous operation has completed.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a>