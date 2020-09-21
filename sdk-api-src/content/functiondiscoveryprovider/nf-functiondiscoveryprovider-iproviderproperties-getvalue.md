---
UID: NF:functiondiscoveryprovider.IProviderProperties.GetValue
title: IProviderProperties::GetValue (functiondiscoveryprovider.h)
description: Gets the value of the specified property key.
helpviewer_keywords: ["GetValue","GetValue method","GetValue method","IProviderProperties interface","IProviderProperties interface","GetValue method","IProviderProperties.GetValue","IProviderProperties::GetValue","functiondiscoveryprovider/IProviderProperties::GetValue","ncd.iproviderproperties_getvalue_method"]
old-location: ncd\iproviderproperties_getvalue_method.htm
tech.root: ncd
ms.assetid: c32a5367-ef39-4852-bf3b-203d27d0a2d0
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method, GetValue method,IProviderProperties interface, IProviderProperties interface,GetValue method, IProviderProperties.GetValue, IProviderProperties::GetValue, functiondiscoveryprovider/IProviderProperties::GetValue, ncd.iproviderproperties_getvalue_method
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
 - IProviderProperties::GetValue
 - functiondiscoveryprovider/IProviderProperties::GetValue
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
 - IProviderProperties.GetValue
---

# IProviderProperties::GetValue


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the value of the specified property key.

## -parameters

### -param pIFunctionInstance [in]

An <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface pointer.

### -param iProviderInstanceContext [in]

The context associated with the specific function instance.

### -param Key [in]

The property key reference.

### -param ppropVar [out]

The value of the property key specified by <i>Key</i>. The <b>PROPVARIANT</b> type is VT_EMPTY if the key is not found in the property store.

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
<i>ppropVar</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate enough memory to perform the operation.

</td>
</tr>
</table>

## -remarks

To change the value of a property key, use the <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderproperties-setvalue">SetValue</a> method.

If a value for <i>Key</i> could not be found, the return value will be <b>S_OK</b> and <i>ppropVar</i> will be set to <b>VT_NULL</b>.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderproperties">IProviderProperties</a>