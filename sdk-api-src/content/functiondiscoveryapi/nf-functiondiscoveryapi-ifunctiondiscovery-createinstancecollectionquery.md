---
UID: NF:functiondiscoveryapi.IFunctionDiscovery.CreateInstanceCollectionQuery
title: IFunctionDiscovery::CreateInstanceCollectionQuery method
author: windows-driver-content
description: Creates a query for a collection of specific function instances.
old-location: ncd\ifunctiondiscovery_createinstancecollectionquery_method.htm
old-project: FunDisc
ms.assetid: 46f74e55-8060-4f02-85e3-dbd2fc8fce78
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CreateInstanceCollectionQuery method, CreateInstanceCollectionQuery method, IFunctionDiscovery interface, CreateInstanceCollectionQuery,IFunctionDiscovery.CreateInstanceCollectionQuery, IFunctionDiscovery, IFunctionDiscovery interface, CreateInstanceCollectionQuery method, IFunctionDiscovery::CreateInstanceCollectionQuery, functiondiscoveryapi/IFunctionDiscovery::CreateInstanceCollectionQuery, ncd.ifunctiondiscovery_createinstancecollectionquery_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: SystemVisibilityFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FunDisc.dll
api_name:
-	IFunctionDiscovery.CreateInstanceCollectionQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: FunDisc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFunctionDiscovery::CreateInstanceCollectionQuery method


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a query for a collection of specific function instances.


## -parameters




### -param pszCategory [in]

The category for the query. See <a href="https://msdn.microsoft.com/84633d91-d193-437c-b1cf-9bc491ad416c">Category Definitions</a>.


### -param pszSubCategory [in]

The subcategory for the query. See <a href="https://msdn.microsoft.com/9793e37d-6c12-431f-95d6-fd5350f11029">Subcategory Definitions</a>. This parameter can be <b>NULL</b>.

Subcategory queries are only supported for layered categories and some provider categories. The <a href="https://msdn.microsoft.com/335b11f1-99f3-42ab-ba22-681f572da246">Registry Provider</a>, the PnP-X association provider, and the publication provider support subcategory queries. Custom providers can be explicitly designed to support subcategory queries. This means the  <i>pszSubCategory</i> parameter should be set to a non-<b>NULL</b> value only when the <i>pszCategory</i> parameter is set to <b>FCTN_CATEGORY_REGISTRY</b>, <b>FCTN_CATEGORY_PUBLICATION</b>, <b>FCTN_CATEGORY_PNPXASSOCIATION</b>, or a custom category value defined for either a layered category or a custom provider supporting subcategory queries.


### -param fIncludeAllSubCategories [in]

If <b>TRUE</b>, this method recursively creates a query for all the subcategories of the category specified in <i>pszCategory</i>, returning a collection containing function instances from all the subcategories of <i>pszCategory</i>. 



If <b>FALSE</b>, this method restricts the created query to returning function instances in the category specified by <i>pszCategory</i> and the subcategory specified by <i>pszSubCategory</i>.


### -param pIFunctionDiscoveryNotification [in]

A pointer to the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface implemented by the calling application. This parameter can be <b>NULL</b>. This pointer is valid until the returned query object is released.


### -param pfdqcQueryContext [in, out]

A pointer to the context in which the query was created. The type <b>FDQUERYCONTEXT</b> is defined as a DWORDLONG. 


### -param ppIFunctionInstanceCollectionQuery [out]

A pointer to the <a href="https://msdn.microsoft.com/ae279ac1-ed7a-431b-a5aa-d60f5f9a64b0">IFunctionInstanceCollectionQuery</a> interface pointer.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code/value</th>
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
The value of <i>pszCategory</i> or <i>pIID</i> is invalid.  The value returned in <i>ppIFunctionInstanceCollectionQuery</i> parameter is <b>NULL</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
<dt>0x80070002</dt>
</dl>
</td>
<td width="60%">
The value of <i>pszCategory</i> or <i>pszSubCategory</i> is unknown.

</td>
</tr>
</table>
 




## -remarks



If <i>pIFunctionDiscoveryNotification</i> is specified, it enables the Function Discovery change notification process. This parameter can be <b>NULL</b>. However, it is required for network providers since they do not return synchronous results. Function Discovery network providers only return instances through the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface.

This method only initializes the query call. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff543208">Execute</a> method of the <a href="https://msdn.microsoft.com/ae279ac1-ed7a-431b-a5aa-d60f5f9a64b0">IFunctionInstanceCollectionQuery</a> interface returned in <i>ppIFunctionInstanceCollectionQuery</i> must be called to perform the query and return any data.




## -see-also




<a href="https://msdn.microsoft.com/3c255fb4-8f9d-47a2-9770-1aa528d07f43">Function Discovery Queries</a>



<a href="https://msdn.microsoft.com/352a8d61-7d3a-423d-8b7e-1163d4fa1e00">IFunctionDiscovery</a>
 

 

