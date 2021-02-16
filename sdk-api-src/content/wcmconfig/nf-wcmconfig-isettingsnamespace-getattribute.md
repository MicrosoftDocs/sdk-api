---
UID: NF:wcmconfig.ISettingsNamespace.GetAttribute
title: ISettingsNamespace::GetAttribute (wcmconfig.h)
description: Gets the value of an attribute of the namespace.
helpviewer_keywords: ["GetAttribute","GetAttribute method [SMI]","GetAttribute method [SMI]","ISettingsNamespace interface","ISettingsNamespace interface [SMI]","GetAttribute method","ISettingsNamespace.GetAttribute","ISettingsNamespace::GetAttribute","smi.isettingsnamespace_getattribute","wcmconfig/ISettingsNamespace::GetAttribute"]
old-location: smi\isettingsnamespace_getattribute.htm
tech.root: SMI
ms.assetid: b0623114-8f25-4870-a1c7-4f4e3ecf0348
ms.date: 12/05/2018
ms.keywords: GetAttribute, GetAttribute method [SMI], GetAttribute method [SMI],ISettingsNamespace interface, ISettingsNamespace interface [SMI],GetAttribute method, ISettingsNamespace.GetAttribute, ISettingsNamespace::GetAttribute, smi.isettingsnamespace_getattribute, wcmconfig/ISettingsNamespace::GetAttribute
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISettingsNamespace::GetAttribute
 - wcmconfig/ISettingsNamespace::GetAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsNamespace.GetAttribute
---

# ISettingsNamespace::GetAttribute


## -description

Gets the value of an attribute of the namespace.

## -parameters

### -param Name [in]

The name of the attribute.

### -param Value [out]

The value of the attribute.

## -returns

This method can return one of these values.

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
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the requested attribute  is not specified for the item.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that there are insufficient resources to return information to the user.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsnamespace">ISettingsNamespace</a>