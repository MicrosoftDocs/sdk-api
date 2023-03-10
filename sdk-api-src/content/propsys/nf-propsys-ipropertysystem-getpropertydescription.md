---
UID: NF:propsys.IPropertySystem.GetPropertyDescription
title: IPropertySystem::GetPropertyDescription (propsys.h)
description: Gets an instance of the subsystem object that implements IPropertyDescription, to obtain the property description for a given PROPERTYKEY.
helpviewer_keywords: ["GetPropertyDescription","GetPropertyDescription method [Windows Properties]","GetPropertyDescription method [Windows Properties]","IPropertySystem interface","IPropertySystem interface [Windows Properties]","GetPropertyDescription method","IPropertySystem.GetPropertyDescription","IPropertySystem::GetPropertyDescription","properties.IPropertySystem_GetPropertyDescription","propsys/IPropertySystem::GetPropertyDescription","shell.IPropertySystem_GetPropertyDescription","shell_IPropertySystem_GetPropertyDescription"]
old-location: properties\IPropertySystem_GetPropertyDescription.htm
tech.root: properties
ms.assetid: c26f6f7e-7ed1-4a97-a9b0-63197ee7b43a
ms.date: 12/05/2018
ms.keywords: GetPropertyDescription, GetPropertyDescription method [Windows Properties], GetPropertyDescription method [Windows Properties],IPropertySystem interface, IPropertySystem interface [Windows Properties],GetPropertyDescription method, IPropertySystem.GetPropertyDescription, IPropertySystem::GetPropertyDescription, properties.IPropertySystem_GetPropertyDescription, propsys/IPropertySystem::GetPropertyDescription, shell.IPropertySystem_GetPropertyDescription, shell_IPropertySystem_GetPropertyDescription
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Propsys.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IPropertySystem::GetPropertyDescription
 - propsys/IPropertySystem::GetPropertyDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.dll
api_name:
 - IPropertySystem.GetPropertyDescription
---

# IPropertySystem::GetPropertyDescription


## -description

Gets an instance of the subsystem object that implements <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>, to obtain the property description for a given <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>.

## -parameters

### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

A reference to the desired property key. See <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired IID.

### -param ppv [out]

Type: <b>void**</b>

The address of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

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
Indicates the interface is obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that <i>ppv</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> does not exist in the schema subsystem cache.

</td>
</tr>
</table>

## -remarks

It is recommended that you use the IID_PPV_ARGS macro, defined in objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, eliminating the possibility of a coding error.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertysystem">IPropertySystem</a>