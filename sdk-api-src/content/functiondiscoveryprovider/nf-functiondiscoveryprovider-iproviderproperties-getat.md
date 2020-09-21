---
UID: NF:functiondiscoveryprovider.IProviderProperties.GetAt
title: IProviderProperties::GetAt (functiondiscoveryprovider.h)
description: Gets the property key at the specified index.
helpviewer_keywords: ["GetAt","GetAt method","GetAt method","IProviderProperties interface","IProviderProperties interface","GetAt method","IProviderProperties.GetAt","IProviderProperties::GetAt","functiondiscoveryprovider/IProviderProperties::GetAt","ncd.iproviderproperties_getat_method"]
old-location: ncd\iproviderproperties_getat_method.htm
tech.root: ncd
ms.assetid: f76d010b-f9dd-46d7-9b1f-eba3d11aaef1
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method, GetAt method,IProviderProperties interface, IProviderProperties interface,GetAt method, IProviderProperties.GetAt, IProviderProperties::GetAt, functiondiscoveryprovider/IProviderProperties::GetAt, ncd.iproviderproperties_getat_method
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
 - IProviderProperties::GetAt
 - functiondiscoveryprovider/IProviderProperties::GetAt
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
 - IProviderProperties.GetAt
---

# IProviderProperties::GetAt


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the property key at the specified index.

## -parameters

### -param pIFunctionInstance [in]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface.

### -param iProviderInstanceContext [in]

The context associated with the specific function instance.

### -param dwIndex [in]

The index of the property key.

### -param pKey [out]

The property key.

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
One of the input parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The  <i>pKey</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderproperties">IProviderProperties</a>