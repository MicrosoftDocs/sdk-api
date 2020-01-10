---
UID: NF:shobjidl_core.IPropertyUI.GetPropertyDescription
title: IPropertyUI::GetPropertyDescription (shobjidl_core.h)
description: Developers should use IPropertyDescription instead. Gets the property description of a specified property.
old-location: properties\IPropertyUI_GetPropertyDescription.htm
tech.root: properties
ms.assetid: 47EAA768-BDAE-44de-AAD8-529E12761065
ms.date: 12/05/2018
ms.keywords: GetPropertyDescription, GetPropertyDescription method [Windows Properties], GetPropertyDescription method [Windows Properties],IPropertyUI interface, IPropertyUI interface [Windows Properties],GetPropertyDescription method, IPropertyUI.GetPropertyDescription, IPropertyUI::GetPropertyDescription, _shell_IPropertyUI_GetPropertyDescription, properties.IPropertyUI_GetPropertyDescription, shell.IPropertyUI_GetPropertyDescription, shobjidl_core/IPropertyUI::GetPropertyDescription
f1_keywords:
- shobjidl_core/IPropertyUI.GetPropertyDescription
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shobjidl_core.h
api_name:
- IPropertyUI.GetPropertyDescription
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyUI::GetPropertyDescription


## -description


Developers should use <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> instead. Gets the property description of a specified property.


## -parameters




### -param fmtid [in]

Type: <b>REFFMTID</b>

The FMTID of the property.


### -param pid [in]

Type: <b>PROPID</b>

The PROPID of the property.


### -param pwszText [out]

Type: <b>LPWSTR</b>

The description of the property.


### -param cchText [in]

Type: <b>DWORD</b>

The length of the property description.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



