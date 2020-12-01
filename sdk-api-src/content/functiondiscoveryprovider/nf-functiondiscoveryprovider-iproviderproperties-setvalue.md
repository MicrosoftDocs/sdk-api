---
UID: NF:functiondiscoveryprovider.IProviderProperties.SetValue
title: IProviderProperties::SetValue (functiondiscoveryprovider.h)
description: Sets the value of the specified property key.
helpviewer_keywords: ["IProviderProperties interface","SetValue method","IProviderProperties.SetValue","IProviderProperties::SetValue","SetValue","SetValue method","SetValue method","IProviderProperties interface","functiondiscoveryprovider/IProviderProperties::SetValue","ncd.iproviderproperties_setvalue"]
old-location: ncd\iproviderproperties_setvalue.htm
tech.root: ncd
ms.assetid: 5aa3e6a3-febc-4d2d-b58b-abfad28d325d
ms.date: 12/05/2018
ms.keywords: IProviderProperties interface,SetValue method, IProviderProperties.SetValue, IProviderProperties::SetValue, SetValue, SetValue method, SetValue method,IProviderProperties interface, functiondiscoveryprovider/IProviderProperties::SetValue, ncd.iproviderproperties_setvalue
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
 - IProviderProperties::SetValue
 - functiondiscoveryprovider/IProviderProperties::SetValue
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
 - IProviderProperties.SetValue
---

# IProviderProperties::SetValue


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sets the value of the specified property key.

## -parameters

### -param pIFunctionInstance [in]

An <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface.

### -param iProviderInstanceContext [in]

The context associated with the specific function instance.

### -param Key [in]

The property key for the property to be set.

### -param ppropVar [in]

The property data. To remove the property from the store, specify a <b>PROPVARIANT</b> with the type VT_EMPTY.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pIFunctionInstance</i>, <i>pvProviderInstanceContext</i>, or <i>ppropVar</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderproperties">IProviderProperties</a>