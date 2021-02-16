---
UID: NF:functiondiscoveryapi.IFunctionDiscovery.AddInstance
title: IFunctionDiscovery::AddInstance (functiondiscoveryapi.h)
description: Creates or modifies a function instance.
helpviewer_keywords: ["AddInstance","AddInstance method","AddInstance method","IFunctionDiscovery interface","IFunctionDiscovery interface","AddInstance method","IFunctionDiscovery.AddInstance","IFunctionDiscovery::AddInstance","functiondiscoveryapi/IFunctionDiscovery::AddInstance","ncd.ifunctiondiscovery_addinstance_method"]
old-location: ncd\ifunctiondiscovery_addinstance_method.htm
tech.root: ncd
ms.assetid: a99213b5-b310-4ce2-99ca-07b343f08c4d
ms.date: 12/05/2018
ms.keywords: AddInstance, AddInstance method, AddInstance method,IFunctionDiscovery interface, IFunctionDiscovery interface,AddInstance method, IFunctionDiscovery.AddInstance, IFunctionDiscovery::AddInstance, functiondiscoveryapi/IFunctionDiscovery::AddInstance, ncd.ifunctiondiscovery_addinstance_method
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
 - IFunctionDiscovery::AddInstance
 - functiondiscoveryapi/IFunctionDiscovery::AddInstance
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
 - IFunctionDiscovery.AddInstance
---

# IFunctionDiscovery::AddInstance


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates or modifies a function instance.

## -parameters

### -param enumSystemVisibility [in]

A <a href="/windows/win32/api/functiondiscoveryapi/ne-functiondiscoveryapi-systemvisibilityflags">SystemVisibilityFlags</a> value that specifies whether the created function instance is visible system wide or only to the current user. 

<div class="alert"><b>Note</b>  The function instance is stored in HKEY_LOCAL_MACHINE regardless  of the <i>enumSystemVisibility</i> value. The user must have Administrator access to add a function instance.</div>
<div> </div>

### -param pszCategory [in]

The category of the created function instance. See <a href="/previous-versions/windows/desktop/fundisc/category-definitions">Category Definitions</a>.

### -param pszSubCategory [in]

The subcategory of the created function instance. See <a href="/previous-versions/windows/desktop/fundisc/subcategory-definitions">Subcategory Definitions</a>. The maximum length of this string is MAX_PATH.

### -param pszCategoryIdentity [in]

The provider instance identifier string. This string is returned from <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-getproviderinstanceid">GetProviderInstanceID</a>.

### -param ppIFunctionInstance [out]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a>  interface pointer that receives the function instance.

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
The value of <i>enumSystemVisibility</i>, <i>pszCategory</i>, or <i>pszCategoryIdentity</i> is invalid.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The provider does not support adding function instances directly using the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-addinstance">AddInstance</a> method.

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
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was specified. This error is returned when the length of the <i>pszSubCategory</i> string exceeds MAX_PATH.

</td>
</tr>
</table>

## -remarks

This method temporarily creates a new function instance for the specified category and subcategory.  The provider that implements the category is responsible for persisting the metadata associated with the newly created function instance using the <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory-createinstance">IFunctionDiscoveryProviderFactory::CreateInstance</a> method.

The function instance is not written to the registry if its associated property store does not have any values. Use the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-openpropertystore">IFunctionInstance::OpenPropertyStore</a> method to check the property store values.

If a function instance already exists for the specified category and subcategory, the existing registry entry is overwritten. The <b>AddInstance</b> method returns S_OK. The Function Discovery change notification process invokes the calling application's <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onupdate">IFunctionDiscoveryNotification::OnUpdate</a> method with <i>enumQueryUpdateAction</i> set to <b>QUA_CHANGE</b>.  

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onupdate">IFunctionDiscoveryNotification::OnUpdate</a> method is not supported by any current provider.</div>
<div> </div>
Whether the new function instance is capable of being visible system-wide or only to the user depends on the provider. The registry provider initially sets its default function instance visibility to system wide.

Access permission to change HKEY_LOCAL_MACHINE\SYSTEM registry keys is required in order to add or remove function instances using the registry provider (Administrator or Power User access).

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a>