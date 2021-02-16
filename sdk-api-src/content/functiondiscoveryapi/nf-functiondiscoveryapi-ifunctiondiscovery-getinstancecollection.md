---
UID: NF:functiondiscoveryapi.IFunctionDiscovery.GetInstanceCollection
title: IFunctionDiscovery::GetInstanceCollection (functiondiscoveryapi.h)
description: Gets the specified collection of function instances, based on category and subcategory.
helpviewer_keywords: ["GetInstanceCollection","GetInstanceCollection method","GetInstanceCollection method","IFunctionDiscovery interface","IFunctionDiscovery interface","GetInstanceCollection method","IFunctionDiscovery.GetInstanceCollection","IFunctionDiscovery::GetInstanceCollection","functiondiscoveryapi/IFunctionDiscovery::GetInstanceCollection","ncd.ifunctiondiscovery_getinstancecollection_method"]
old-location: ncd\ifunctiondiscovery_getinstancecollection_method.htm
tech.root: ncd
ms.assetid: 615d252c-7365-4ef5-9e4f-94a49783a1bb
ms.date: 12/05/2018
ms.keywords: GetInstanceCollection, GetInstanceCollection method, GetInstanceCollection method,IFunctionDiscovery interface, IFunctionDiscovery interface,GetInstanceCollection method, IFunctionDiscovery.GetInstanceCollection, IFunctionDiscovery::GetInstanceCollection, functiondiscoveryapi/IFunctionDiscovery::GetInstanceCollection, ncd.ifunctiondiscovery_getinstancecollection_method
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
 - IFunctionDiscovery::GetInstanceCollection
 - functiondiscoveryapi/IFunctionDiscovery::GetInstanceCollection
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
 - IFunctionDiscovery.GetInstanceCollection
---

# IFunctionDiscovery::GetInstanceCollection


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the specified collection of function instances, based on category and subcategory.

## -parameters

### -param pszCategory [in]

The identifier of the category to be enumerated. See <a href="/previous-versions/windows/desktop/fundisc/category-definitions">Category Definitions</a>.

### -param pszSubCategory [in]

The identifier of the subcategory to be enumerated. See <a href="/previous-versions/windows/desktop/fundisc/subcategory-definitions">Subcategory Definitions</a>. This parameter can be <b>NULL</b>.

### -param fIncludeAllSubCategories [in]

If <b>TRUE</b>, this method recursively enumerates all the subcategories of the category specified in <i>pszCategory</i>, returning a collection containing function instances from all the subcategories of <i>pszCategory</i>. 



If <b>FALSE</b>, this method restricts itself to returning function instances in the category specified by <i>pszCategory</i> and the subcategory specified by <i>pszSubCategory</i>.

### -param ppIFunctionInstanceCollection [out]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollection">IFunctionInstanceCollection</a> interface pointer that receives the function instance collection containing the requested function instances. The collection is empty if no qualifying function instances are found.

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
The value of <i>pszCategory</i> is invalid.  The value returned in <i>ppIFunctionInstanceCollection</i> parameter is <b>NULL</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The call was executed for a provider that returns results asynchronously.

</td>
</tr>
</table>

## -remarks

Some function discovery providers return their query results with the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface.  <b>GetInstanceCollection</b> does not find function instances that are returned in this way and will fail with E_PENDING.  It is recommended that clients use the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancequery">CreateInstanceQuery</a> method of the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a> interface to find function instances for such providers.

If the method succeeds but no function instances were found that matched the query parameters, then <b>S_OK</b> is returned and <i>ppFunctionInstanceCollection</i> points to an empty collection (the collection's <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollection-getcount">GetCount</a> method returns 0).

Subcategory queries are only supported for layered categories and some provider categories. The <a href="/previous-versions/windows/desktop/fundisc/registry-provider">Registry Provider</a>, the PnP-X association provider, and the publication provider support subcategory queries. Custom providers can be explicitly designed to support subcategory queries. For other providers, function instance collections can be filtered using query constraints. For a list of query constraints, see <a href="/previous-versions/windows/desktop/fundisc/constraint-definitions">Constraint Definitions</a>.


#### Examples

The following code returns the function instances associated with the SSDP provider in the Microsoft.Networking.Devices namespace.


```cpp
hr = spDisco->GetInstanceCollection(FCTN_CATEGORY_NETWORKDEVICES,
                                   FCTN_SUBCAT_NETWORKDEVICES_SSDP, 
                                   FALSE, 
                                   &spFunctionInstanceCollection);


```


See interface constraints on <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancequery">IFunctionInstanceQuery</a> to filter on multiple interfaces at one time or to filter on providers that do not support subcategory queries.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a>