---
UID: NF:propsys.IPropertySystem.GetPropertyDescriptionByName
title: IPropertySystem::GetPropertyDescriptionByName (propsys.h)
description: Gets an instance of the subsystem object that implements IPropertyDescription, to obtain the property description for a given canonical name.
helpviewer_keywords: ["GetPropertyDescriptionByName","GetPropertyDescriptionByName method [Windows Properties]","GetPropertyDescriptionByName method [Windows Properties]","IPropertySystem interface","IPropertySystem interface [Windows Properties]","GetPropertyDescriptionByName method","IPropertySystem.GetPropertyDescriptionByName","IPropertySystem::GetPropertyDescriptionByName","properties.IPropertySystem_GetPropertyDescriptionByName","propsys/IPropertySystem::GetPropertyDescriptionByName","shell.IPropertySystem_GetPropertyDescriptionByName","shell_IPropertySystem_GetPropertyDescriptionByName"]
old-location: properties\IPropertySystem_GetPropertyDescriptionByName.htm
tech.root: properties
ms.assetid: ec1b3ded-ad7f-4830-92a2-35ad5691aa10
ms.date: 12/05/2018
ms.keywords: GetPropertyDescriptionByName, GetPropertyDescriptionByName method [Windows Properties], GetPropertyDescriptionByName method [Windows Properties],IPropertySystem interface, IPropertySystem interface [Windows Properties],GetPropertyDescriptionByName method, IPropertySystem.GetPropertyDescriptionByName, IPropertySystem::GetPropertyDescriptionByName, properties.IPropertySystem_GetPropertyDescriptionByName, propsys/IPropertySystem::GetPropertyDescriptionByName, shell.IPropertySystem_GetPropertyDescriptionByName, shell_IPropertySystem_GetPropertyDescriptionByName
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
 - IPropertySystem::GetPropertyDescriptionByName
 - propsys/IPropertySystem::GetPropertyDescriptionByName
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
 - IPropertySystem.GetPropertyDescriptionByName
---

# IPropertySystem::GetPropertyDescriptionByName


## -description

Gets an instance of the subsystem object that implements <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>, to obtain the property description for a given canonical name.

## -parameters

### -param pszCanonicalName [in]

Type: <b>LPCWSTR</b>

A pointer to a string that identifies the property.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired IID.

### -param ppv [out]

Type: <b>void**</b>

The address of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> interface pointer.

## -returns

Type: <b>PSSTDAPI</b>

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
Indicates that the interface is obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates <i>pszCanonicalName</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the canonical name does not exist in the schema subsystem cache.

</td>
</tr>
</table>

## -remarks

It is recommended that you use the IID_PPV_ARGS macro, defined in objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, eliminating the possibility of a coding error.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertysystem">IPropertySystem</a>