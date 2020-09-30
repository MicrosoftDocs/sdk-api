---
UID: NF:functiondiscoveryprovider.IProviderPublishing.RemoveInstance
title: IProviderPublishing::RemoveInstance (functiondiscoveryprovider.h)
description: Deletes an existing function instance.
helpviewer_keywords: ["IProviderPublishing interface","RemoveInstance method","IProviderPublishing.RemoveInstance","IProviderPublishing::RemoveInstance","RemoveInstance","RemoveInstance method","RemoveInstance method","IProviderPublishing interface","functiondiscoveryprovider/IProviderPublishing::RemoveInstance","ncd.iproviderpublishing_removeinstance_method"]
old-location: ncd\iproviderpublishing_removeinstance_method.htm
tech.root: ncd
ms.assetid: 7b4f6122-944e-4fe9-be95-dd09ae1542f1
ms.date: 12/05/2018
ms.keywords: IProviderPublishing interface,RemoveInstance method, IProviderPublishing.RemoveInstance, IProviderPublishing::RemoveInstance, RemoveInstance, RemoveInstance method, RemoveInstance method,IProviderPublishing interface, functiondiscoveryprovider/IProviderPublishing::RemoveInstance, ncd.iproviderpublishing_removeinstance_method
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
 - IProviderPublishing::RemoveInstance
 - functiondiscoveryprovider/IProviderPublishing::RemoveInstance
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
 - IProviderPublishing.RemoveInstance
---

# IProviderPublishing::RemoveInstance


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Deletes an existing function instance.

## -parameters

### -param enumVisibilityFlags [in]

A <a href="/windows/win32/api/functiondiscoveryapi/ne-functiondiscoveryapi-systemvisibilityflags">SystemVisibilityFlags</a> enumeration value which specifies the visibility of the function instance which the provider is about to delete.  It is up to the provider whether or not to honor this setting, however the current user visibility can be used to allow processes running in a non-Administrator security context to still be able to remove function instances.

### -param pszSubCategory [in]

The subcategory string of the function instance.

### -param pszProviderInstanceIdentity [in]

The provider instance identifier.

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
The <i>pSiteInfo</i>, <i>pszSubCategory</i>, or <i>pszProviderInstanceIdentity</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderpublishing">IProviderPublishing</a>