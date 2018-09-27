---
UID: NF:functiondiscoveryapi.IFunctionDiscovery.RemoveInstance
title: IFunctionDiscovery::RemoveInstance
author: windows-sdk-content
description: Removes the specified function instance, based on category and subcategory.
old-location: ncd\ifunctiondiscovery_removeinstance_method.htm
tech.root: fundisc
ms.assetid: 743ec310-ea35-4c4b-92f0-bbfe0a2f6f30
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IFunctionDiscovery interface,RemoveInstance method, IFunctionDiscovery.RemoveInstance, IFunctionDiscovery::RemoveInstance, RemoveInstance, RemoveInstance method, RemoveInstance method,IFunctionDiscovery interface, functiondiscoveryapi/IFunctionDiscovery::RemoveInstance, ncd.ifunctiondiscovery_removeinstance_method
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
req.lib: 
req.dll: FunDisc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionDiscovery.RemoveInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionDiscovery::RemoveInstance


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Removes the specified function instance, based on category and subcategory.


## -parameters




### -param enumSystemVisibility [in]

A <a href="https://msdn.microsoft.com/a3388293-150c-417a-a4a6-0d5020e0ae82">SystemVisibilityFlags</a> value that specifies whether the function instance is removed system-wide or only for the current user. 


### -param pszCategory [in]

The category of the function instance. See <a href="https://msdn.microsoft.com/84633d91-d193-437c-b1cf-9bc491ad416c">Category Definitions</a>.


### -param pszSubCategory [in]

The subcategory of the function instance to be removed.  See <a href="https://msdn.microsoft.com/9793e37d-6c12-431f-95d6-fd5350f11029">Subcategory Definitions</a>. This parameter can be <b>NULL</b>.


### -param pszCategoryIdentity [in]

The provider instance identifier string. This string is returned from <a href="https://msdn.microsoft.com/fad5e3f0-a440-4b09-ba8c-04bae2d14a2a">GetProviderInstanceID</a>.


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




<a href="https://msdn.microsoft.com/352a8d61-7d3a-423d-8b7e-1163d4fa1e00">IFunctionDiscovery</a>
 

 

