---
UID: NF:functiondiscoveryapi.IFunctionDiscoveryNotification.OnError
title: IFunctionDiscoveryNotification::OnError (functiondiscoveryapi.h)
description: Receives errors that occur during asynchronous query processing.
helpviewer_keywords: ["IFunctionDiscoveryNotification interface","OnError method","IFunctionDiscoveryNotification.OnError","IFunctionDiscoveryNotification::OnError","OnError","OnError method","OnError method","IFunctionDiscoveryNotification interface","functiondiscoveryapi/IFunctionDiscoveryNotification::OnError","ncd.ifunctiondiscoverynotification_onerror"]
old-location: ncd\ifunctiondiscoverynotification_onerror.htm
tech.root: ncd
ms.assetid: c4dcc4e9-7acf-44d3-b337-1ac01afa19b0
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryNotification interface,OnError method, IFunctionDiscoveryNotification.OnError, IFunctionDiscoveryNotification::OnError, OnError, OnError method, OnError method,IFunctionDiscoveryNotification interface, functiondiscoveryapi/IFunctionDiscoveryNotification::OnError, ncd.ifunctiondiscoverynotification_onerror
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFunctionDiscoveryNotification::OnError
 - functiondiscoveryapi/IFunctionDiscoveryNotification::OnError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - functiondiscoveryapi.h
api_name:
 - IFunctionDiscoveryNotification.OnError
---

# IFunctionDiscoveryNotification::OnError


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Receives errors that occur during asynchronous query processing.

## -parameters

### -param hr [in]

The query error that is being reported.

### -param fdqcQueryContext [in]

The context registered for change notification. The type <b>FDQUERYCONTEXT</b> is defined as a DWORDLONG.

### -param pszProvider [in]

The name of the provider.

## -returns

The client program's implementation of the <b>OnError</b> method should return one of the following <b>HRESULT</b> values to the caller.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of one of the input parameters is invalid.

</td>
</tr>
</table>

## -remarks

Typically, clients will expect that any asynchronous error is fatal and that the query will stop returning results, but custom provider documentation could indicate otherwise for specific error codes.

Do not call <b>Release</b> on the query object from this method. Doing so could cause a deadlock. If <b>Release</b>  is called on a query object from another thread while a callback is in process, the object will not be released until the callback has finished.

All notifications passed to Function Discovery by providers are queued and returned to the client one by one. Callbacks are synchronized so that a client will only receive one notification at a time.

Because other <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> method calls may be made in other threads, any changes made to the thread state during the call  must be restored before exiting the method.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a>