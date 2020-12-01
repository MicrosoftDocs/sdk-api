---
UID: NF:functiondiscoveryapi.IFunctionDiscovery.CreateInstanceQuery
title: IFunctionDiscovery::CreateInstanceQuery (functiondiscoveryapi.h)
description: Creates a query for a specific function instance.
helpviewer_keywords: ["CreateInstanceQuery","CreateInstanceQuery method","CreateInstanceQuery method","IFunctionDiscovery interface","IFunctionDiscovery interface","CreateInstanceQuery method","IFunctionDiscovery.CreateInstanceQuery","IFunctionDiscovery::CreateInstanceQuery","functiondiscoveryapi/IFunctionDiscovery::CreateInstanceQuery","ncd.ifunctiondiscovery_createinstancequery_method"]
old-location: ncd\ifunctiondiscovery_createinstancequery_method.htm
tech.root: ncd
ms.assetid: 80e70972-ced1-416e-aa4f-69c54b2cbf95
ms.date: 12/05/2018
ms.keywords: CreateInstanceQuery, CreateInstanceQuery method, CreateInstanceQuery method,IFunctionDiscovery interface, IFunctionDiscovery interface,CreateInstanceQuery method, IFunctionDiscovery.CreateInstanceQuery, IFunctionDiscovery::CreateInstanceQuery, functiondiscoveryapi/IFunctionDiscovery::CreateInstanceQuery, ncd.ifunctiondiscovery_createinstancequery_method
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
req.dll: FunDisc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFunctionDiscovery::CreateInstanceQuery
 - functiondiscoveryapi/IFunctionDiscovery::CreateInstanceQuery
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionDiscovery.CreateInstanceQuery
---

# IFunctionDiscovery::CreateInstanceQuery


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a query for a specific function instance.

## -parameters

### -param pszFunctionInstanceIdentity [in]

The identifier of the function instance.

### -param pIFunctionDiscoveryNotification [in]

A pointer to the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface implemented by the calling application. If specified, it enables the Function Discovery change notification process. This parameter can be <b>NULL</b>; however it is required for network providers.

### -param pfdqcQueryContext [in, out]

A pointer to the context in which the query was created. The type <b>FDQUERYCONTEXT</b> is defined as a DWORDLONG.

### -param ppIFunctionInstanceQuery [out]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancequery">IFunctionInstanceQuery</a> interface pointer used to return the generated query.

## -returns

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
<i>ppIFunctionInstanceQuery</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to perform this operation.

</td>
</tr>
</table>

## -remarks

Function Discovery Network providers only return instances through the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface.

This method only initializes the query call. The <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancequery-execute">Execute</a> method of the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancequery">IFunctionInstanceQuery</a> interface returned in <i>ppIFunctionInstanceQuery</i> must be called to perform the query and return any data.

## -see-also

<a href="/previous-versions/windows/desktop/fundisc/function-discovery-queries">Function Discovery Queries</a>



<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a>