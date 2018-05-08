---
UID: NF:functiondiscoveryapi.IFunctionDiscovery.AddInstance
title: IFunctionDiscovery::AddInstance
author: windows-driver-content
description: Creates or modifies a function instance.
old-location: ncd\ifunctiondiscovery_addinstance_method.htm
old-project: FunDisc
ms.assetid: a99213b5-b310-4ce2-99ca-07b343f08c4d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: AddInstance, AddInstance method, AddInstance method,IFunctionDiscovery interface, IFunctionDiscovery interface,AddInstance method, IFunctionDiscovery.AddInstance, IFunctionDiscovery::AddInstance, functiondiscoveryapi/IFunctionDiscovery::AddInstance, ncd.ifunctiondiscovery_addinstance_method
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
-	IFunctionDiscovery.AddInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: FunDisc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFunctionDiscovery::AddInstance


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates or modifies a function instance.


## -parameters




### -param enumSystemVisibility [in]

A <a href="https://msdn.microsoft.com/a3388293-150c-417a-a4a6-0d5020e0ae82">SystemVisibilityFlags</a> value that specifies whether the created function instance is visible system wide or only to the current user. 

<div class="alert"><b>Note</b>  The function instance is stored in HKEY_LOCAL_MACHINE regardless  of the <i>enumSystemVisibility</i> value. The user must have Administrator access to add a function instance.</div>
<div> </div>

### -param pszCategory [in]

The category of the created function instance. See <a href="https://msdn.microsoft.com/84633d91-d193-437c-b1cf-9bc491ad416c">Category Definitions</a>.


### -param pszSubCategory [in]

The subcategory of the created function instance. See <a href="https://msdn.microsoft.com/9793e37d-6c12-431f-95d6-fd5350f11029">Subcategory Definitions</a>. The maximum length of this string is MAX_PATH.


### -param pszCategoryIdentity [in]

The provider instance identifier string. This string is returned from <a href="https://msdn.microsoft.com/fad5e3f0-a440-4b09-ba8c-04bae2d14a2a">GetProviderInstanceID</a>.


### -param ppIFunctionInstance [out]

A pointer to an <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a>  interface pointer that receives the function instance.


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
The provider does not support adding function instances directly using the <a href="https://msdn.microsoft.com/a99213b5-b310-4ce2-99ca-07b343f08c4d">AddInstance</a> method.

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



This method temporarily creates a new function instance for the specified category and subcategory.  The provider that implements the category is responsible for persisting the metadata associated with the newly created function instance using the <a href="https://msdn.microsoft.com/143a4f62-7093-4127-b89e-e7d0985a92bb">IFunctionDiscoveryProviderFactory::CreateInstance</a> method.

The function instance is not written to the registry if its associated property store does not have any values. Use the <a href="https://msdn.microsoft.com/3e03567b-7bac-4bef-ae62-a040f0c33cfb">IFunctionInstance::OpenPropertyStore</a> method to check the property store values.

If a function instance already exists for the specified category and subcategory, the existing registry entry is overwritten. The <b>AddInstance</b> method returns S_OK. The Function Discovery change notification process invokes the calling application's <a href="https://msdn.microsoft.com/ab4d0fc6-de3f-49cf-b53c-573222a8bc89">IFunctionDiscoveryNotification::OnUpdate</a> method with <i>enumQueryUpdateAction</i> set to <b>QUA_CHANGE</b>.  

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/ab4d0fc6-de3f-49cf-b53c-573222a8bc89">IFunctionDiscoveryNotification::OnUpdate</a> method is not supported by any current provider.</div>
<div> </div>
Whether the new function instance is capable of being visible system-wide or only to the user depends on the provider. The registry provider initially sets its default function instance visibility to system wide.

Access permission to change HKEY_LOCAL_MACHINE\SYSTEM registry keys is required in order to add or remove function instances using the registry provider (Administrator or Power User access).




## -see-also




<a href="https://msdn.microsoft.com/352a8d61-7d3a-423d-8b7e-1163d4fa1e00">IFunctionDiscovery</a>
 

 

