---
UID: NF:functiondiscoveryprovider.IProviderPublishing.CreateInstance
title: IProviderPublishing::CreateInstance
author: windows-sdk-content
description: Creates a new function instance.
old-location: ncd\iproviderpublishing_createinstance_method.htm
old-project: fundisc
ms.assetid: 1c8988d0-552a-434b-b33c-31017a191896
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateInstance, CreateInstance method, CreateInstance method,IProviderPublishing interface, IProviderPublishing interface,CreateInstance method, IProviderPublishing.CreateInstance, IProviderPublishing::CreateInstance, functiondiscoveryprovider/IProviderPublishing::CreateInstance, ncd.iproviderpublishing_createinstance_method, ncd.iproviderpublishing_oncreateinstance_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: PropertyConstraint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IProviderPublishing.CreateInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IProviderPublishing::CreateInstance


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a new function instance.


## -parameters




### -param enumVisibilityFlags [in]

A <a href="https://msdn.microsoft.com/a3388293-150c-417a-a4a6-0d5020e0ae82">SystemVisibilityFlags</a> enumeration value that specifies the visibility of the function instance which the provider is about to create.  It is up to the provider whether or not to honor this flag, however the current user visibility can be used to allow processes running in a non-Administrator security context to still be able to add function instances.


### -param pszSubCategory [in]

The subcategory string for the function instance.


### -param pszProviderInstanceIdentity [in]

The provider instance identifier.


### -param ppIFunctionInstance [out]

A pointer to an <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface pointer used to return the newly created function instance.


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




<a href="https://msdn.microsoft.com/7647db1b-88c8-44f3-b2af-a61dad4790f6">IProviderPublishing</a>
 

 

