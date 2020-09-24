---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollectionQuery.AddPropertyConstraint
title: IFunctionInstanceCollectionQuery::AddPropertyConstraint (functiondiscoveryapi.h)
description: Adds a property constraint to the query.
helpviewer_keywords: ["AddPropertyConstraint","AddPropertyConstraint method","AddPropertyConstraint method","IFunctionInstanceCollectionQuery interface","IFunctionInstanceCollectionQuery interface","AddPropertyConstraint method","IFunctionInstanceCollectionQuery.AddPropertyConstraint","IFunctionInstanceCollectionQuery::AddPropertyConstraint","functiondiscoveryapi/IFunctionInstanceCollectionQuery::AddPropertyConstraint","ncd.ifunctioninstancecollectionquery_addpropertyconstraint_method"]
old-location: ncd\ifunctioninstancecollectionquery_addpropertyconstraint_method.htm
tech.root: ncd
ms.assetid: 4ff850a8-3208-4fb4-a581-7581e71f34e6
ms.date: 12/05/2018
ms.keywords: AddPropertyConstraint, AddPropertyConstraint method, AddPropertyConstraint method,IFunctionInstanceCollectionQuery interface, IFunctionInstanceCollectionQuery interface,AddPropertyConstraint method, IFunctionInstanceCollectionQuery.AddPropertyConstraint, IFunctionInstanceCollectionQuery::AddPropertyConstraint, functiondiscoveryapi/IFunctionInstanceCollectionQuery::AddPropertyConstraint, ncd.ifunctioninstancecollectionquery_addpropertyconstraint_method
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
 - IFunctionInstanceCollectionQuery::AddPropertyConstraint
 - functiondiscoveryapi/IFunctionInstanceCollectionQuery::AddPropertyConstraint
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
 - IFunctionInstanceCollectionQuery.AddPropertyConstraint
---

# IFunctionInstanceCollectionQuery::AddPropertyConstraint


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Adds a property constraint to the query.

This method limits query results to only function instances with a property key (PKEY) matching the specified constraint.

## -parameters

### -param Key [in]

The property key (PKEY) for the constraint. For more information about PKEYs, see <a href="/previous-versions/windows/desktop/fundisc/key-definitions">Key Definitions</a>.

### -param pv [in]

A <b>PROPVARIANT</b> used for the constraint. This type must match the PROPVARIANT type associated with <i>Key</i>.


The following shows possible values. Note that only a subset of the PROPVARIANT types supported by the built-in providers can be used as a property constraint. 



<p class="indent">VT_BOOL

<p class="indent">VT_I2

<p class="indent">VT_I4

<p class="indent">VT_I8

<p class="indent">VT_INT

<p class="indent">VT_LPWSTR

<p class="indent">VT_LPWSTR|VT_VECTOR

<p class="indent">VT_UI2

<p class="indent">VT_UI4

<p class="indent">VT_UI8

<p class="indent">VT_UINT

### -param enumPropertyConstraint [in]

A <a href="/windows/win32/api/functiondiscoveryconstraints/ne-functiondiscoveryconstraints-propertyconstraint">PropertyConstraint</a> value that specifies the type of comparison to use when comparing the constraint's PKEY to the function instance's PKEY.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The constraint specified for the query is not supported.  Either the constraint is not supported for a specific <b>VARENUM</b> type, or the <b>VARENUM</b> type is not supported at all. 

</td>
</tr>
</table>

## -remarks

A function instance will only match a property constraint when the PROPVARIANT type of the function instance's PKEY matches the PROPVARIANT type of the constraint's  PKEY and the function instance's PKEY value matches the constraint's PKEY value using the comparison operator specified by <i>enumPropertyConstraint</i>.

If multiple constraints are added, all constraints must be supported to satisfy the query.

## -see-also

<a href="/previous-versions/windows/desktop/fundisc/function-discovery-queries">Function Discovery Queries</a>



<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollectionquery">IFunctionInstanceCollectionQuery</a>