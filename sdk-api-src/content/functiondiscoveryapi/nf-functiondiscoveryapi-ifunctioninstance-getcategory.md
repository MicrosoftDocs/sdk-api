---
UID: NF:functiondiscoveryapi.IFunctionInstance.GetCategory
title: IFunctionInstance::GetCategory (functiondiscoveryapi.h)
description: Gets the category and subcategory strings for the function instance.
helpviewer_keywords: ["GetCategory","GetCategory method","GetCategory method","IFunctionInstance interface","IFunctionInstance interface","GetCategory method","IFunctionInstance.GetCategory","IFunctionInstance::GetCategory","functiondiscoveryapi/IFunctionInstance::GetCategory","ncd.ifunctioninstance_getcategory_method"]
old-location: ncd\ifunctioninstance_getcategory_method.htm
tech.root: ncd
ms.assetid: dfb5f144-c9b0-455e-aff9-0c07225a21f6
ms.date: 12/05/2018
ms.keywords: GetCategory, GetCategory method, GetCategory method,IFunctionInstance interface, IFunctionInstance interface,GetCategory method, IFunctionInstance.GetCategory, IFunctionInstance::GetCategory, functiondiscoveryapi/IFunctionInstance::GetCategory, ncd.ifunctioninstance_getcategory_method
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
 - IFunctionInstance::GetCategory
 - functiondiscoveryapi/IFunctionInstance::GetCategory
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
 - IFunctionInstance.GetCategory
---

# IFunctionInstance::GetCategory


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the category and subcategory strings for the function instance.

## -parameters

### -param ppszCoMemCategory [out]

The null-terminated identifier string of the category. See <a href="/previous-versions/windows/desktop/fundisc/category-definitions">Category Definitions</a>.

Be sure to free this buffer using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param ppszCoMemSubCategory [out]

The null-terminated identifier string of the subcategory. See <a href="/previous-versions/windows/desktop/fundisc/subcategory-definitions">Subcategory Definitions</a>.

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

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a>