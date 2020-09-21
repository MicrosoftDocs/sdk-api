---
UID: NF:functiondiscoveryapi.IFunctionDiscovery.RemoveInstance
title: IFunctionDiscovery::RemoveInstance (functiondiscoveryapi.h)
description: Removes the specified function instance, based on category and subcategory.
helpviewer_keywords: ["IFunctionDiscovery interface","RemoveInstance method","IFunctionDiscovery.RemoveInstance","IFunctionDiscovery::RemoveInstance","RemoveInstance","RemoveInstance method","RemoveInstance method","IFunctionDiscovery interface","functiondiscoveryapi/IFunctionDiscovery::RemoveInstance","ncd.ifunctiondiscovery_removeinstance_method"]
old-location: ncd\ifunctiondiscovery_removeinstance_method.htm
tech.root: ncd
ms.assetid: 743ec310-ea35-4c4b-92f0-bbfe0a2f6f30
ms.date: 12/05/2018
ms.keywords: IFunctionDiscovery interface,RemoveInstance method, IFunctionDiscovery.RemoveInstance, IFunctionDiscovery::RemoveInstance, RemoveInstance, RemoveInstance method, RemoveInstance method,IFunctionDiscovery interface, functiondiscoveryapi/IFunctionDiscovery::RemoveInstance, ncd.ifunctiondiscovery_removeinstance_method
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
 - IFunctionDiscovery::RemoveInstance
 - functiondiscoveryapi/IFunctionDiscovery::RemoveInstance
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
 - IFunctionDiscovery.RemoveInstance
---

# IFunctionDiscovery::RemoveInstance


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Removes the specified function instance, based on category and subcategory.

## -parameters

### -param enumSystemVisibility [in]

A <a href="/windows/win32/api/functiondiscoveryapi/ne-functiondiscoveryapi-systemvisibilityflags">SystemVisibilityFlags</a> value that specifies whether the function instance is removed system-wide or only for the current user.

### -param pszCategory [in]

The category of the function instance. See <a href="/previous-versions/windows/desktop/fundisc/category-definitions">Category Definitions</a>.

### -param pszSubCategory [in]

The subcategory of the function instance to be removed.  See <a href="/previous-versions/windows/desktop/fundisc/subcategory-definitions">Subcategory Definitions</a>. This parameter can be <b>NULL</b>.

### -param pszCategoryIdentity [in]

The provider instance identifier string. This string is returned from <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-getproviderinstanceid">GetProviderInstanceID</a>.

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
The value of <i>pszCategoryIdentity</i> is invalid.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The user has insufficient access permission to perform the requested action.

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

Access permission to change HKEY_LOCAL_MACHINE\SYSTEM registry keys is required in order to add or remove function instances using the registry provider (Administrator or Power User access levels). The user must have Administrator access to remove a function instance system-wide.

<div class="alert"><b>Note</b>  This method is not supported by all providers.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a>