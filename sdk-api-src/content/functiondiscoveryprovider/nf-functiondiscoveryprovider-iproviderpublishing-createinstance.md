---
UID: NF:functiondiscoveryprovider.IProviderPublishing.CreateInstance
title: IProviderPublishing::CreateInstance (functiondiscoveryprovider.h)
description: Creates a new function instance.
helpviewer_keywords: ["CreateInstance","CreateInstance method","CreateInstance method","IProviderPublishing interface","IProviderPublishing interface","CreateInstance method","IProviderPublishing.CreateInstance","IProviderPublishing::CreateInstance","functiondiscoveryprovider/IProviderPublishing::CreateInstance","ncd.iproviderpublishing_createinstance_method","ncd.iproviderpublishing_oncreateinstance_method"]
old-location: ncd\iproviderpublishing_createinstance_method.htm
tech.root: ncd
ms.assetid: 1c8988d0-552a-434b-b33c-31017a191896
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method, CreateInstance method,IProviderPublishing interface, IProviderPublishing interface,CreateInstance method, IProviderPublishing.CreateInstance, IProviderPublishing::CreateInstance, functiondiscoveryprovider/IProviderPublishing::CreateInstance, ncd.iproviderpublishing_createinstance_method, ncd.iproviderpublishing_oncreateinstance_method
req.header: functiondiscoveryprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
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
 - IProviderPublishing::CreateInstance
 - functiondiscoveryprovider/IProviderPublishing::CreateInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IProviderPublishing.CreateInstance
---

# IProviderPublishing::CreateInstance


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a new function instance.

## -parameters

### -param enumVisibilityFlags [in]

A <a href="/windows/win32/api/functiondiscoveryapi/ne-functiondiscoveryapi-systemvisibilityflags">SystemVisibilityFlags</a> enumeration value that specifies the visibility of the function instance which the provider is about to create.  It is up to the provider whether or not to honor this flag, however the current user visibility can be used to allow processes running in a non-Administrator security context to still be able to add function instances.

### -param pszSubCategory [in]

The subcategory string for the function instance.

### -param pszProviderInstanceIdentity [in]

The provider instance identifier.

### -param ppIFunctionInstance [out]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface pointer used to return the newly created function instance.

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
One of the parameters contains an invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszSubCategory</i>, <i>pszProviderInstanceIdentity</i>, or <i>ppInstance</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderpublishing">IProviderPublishing</a>