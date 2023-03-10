---
UID: NF:functiondiscoveryapi.IFunctionInstance.GetProviderInstanceID
title: IFunctionInstance::GetProviderInstanceID (functiondiscoveryapi.h)
description: Gets the identifier string for the provider instance.
helpviewer_keywords: ["GetProviderInstanceID","GetProviderInstanceID method","GetProviderInstanceID method","IFunctionInstance interface","IFunctionInstance interface","GetProviderInstanceID method","IFunctionInstance.GetProviderInstanceID","IFunctionInstance::GetProviderInstanceID","functiondiscoveryapi/IFunctionInstance::GetProviderInstanceID","ncd.ifunctioninstance_getproviderinstanceid_method"]
old-location: ncd\ifunctioninstance_getproviderinstanceid_method.htm
tech.root: ncd
ms.assetid: fad5e3f0-a440-4b09-ba8c-04bae2d14a2a
ms.date: 12/05/2018
ms.keywords: GetProviderInstanceID, GetProviderInstanceID method, GetProviderInstanceID method,IFunctionInstance interface, IFunctionInstance interface,GetProviderInstanceID method, IFunctionInstance.GetProviderInstanceID, IFunctionInstance::GetProviderInstanceID, functiondiscoveryapi/IFunctionInstance::GetProviderInstanceID, ncd.ifunctioninstance_getproviderinstanceid_method
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
 - IFunctionInstance::GetProviderInstanceID
 - functiondiscoveryapi/IFunctionInstance::GetProviderInstanceID
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
 - IFunctionInstance.GetProviderInstanceID
---

# IFunctionInstance::GetProviderInstanceID


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the identifier string for the provider instance. This string is the unique identifier for the provider instance.

## -parameters

### -param ppszCoMemProviderInstanceIdentity [out]

The provider instance identifier string. For root devices, this string has the same value as PKEY_PNPX_GlobalIdentity.

Be sure to free this buffer using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

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
The value of <i>ppszCoMemProviderInstanceID</i> is invalid.

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

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a>