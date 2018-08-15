---
UID: NF:functiondiscoveryapi.IFunctionInstance.GetCategory
title: IFunctionInstance::GetCategory
author: windows-sdk-content
description: Gets the category and subcategory strings for the function instance.
old-location: ncd\ifunctioninstance_getcategory_method.htm
old-project: fundisc
ms.assetid: dfb5f144-c9b0-455e-aff9-0c07225a21f6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCategory, GetCategory method, GetCategory method,IFunctionInstance interface, IFunctionInstance interface,GetCategory method, IFunctionInstance.GetCategory, IFunctionInstance::GetCategory, functiondiscoveryapi/IFunctionInstance::GetCategory, ncd.ifunctioninstance_getcategory_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: functiondiscoveryapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SystemVisibilityFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionInstance.GetCategory
product: Windows
targetos: Windows
req.lib: 
req.dll: FunDisc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFunctionInstance::GetCategory


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the category and subcategory strings for the function instance.


## -parameters




### -param ppszCoMemCategory [out]

The null-terminated identifier string of the category. See <a href="https://msdn.microsoft.com/84633d91-d193-437c-b1cf-9bc491ad416c">Category Definitions</a>.

Be sure to free this buffer using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a>.


### -param ppszCoMemSubCategory [out]

The null-terminated identifier string of the subcategory. See <a href="https://msdn.microsoft.com/9793e37d-6c12-431f-95d6-fd5350f11029">Subcategory Definitions</a>.


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
</table>
 




## -remarks



The category and subcategory of a function instance always refer to the provider category from which a function instance comes.




## -see-also




<a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a>
 

 

