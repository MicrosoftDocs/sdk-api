---
UID: NF:propsys.IPropertyDescription.GetEnumTypeList
title: IPropertyDescription::GetEnumTypeList (propsys.h)
description: Gets an instance of an IPropertyEnumTypeList, which can be used to enumerate the possible values for a property.
old-location: properties\IPropertyDescription_GetEnumTypeList.htm
tech.root: properties
ms.assetid: ab6c41c2-d85c-4ff9-9061-043303eb1a83
ms.date: 12/05/2018
ms.keywords: GetEnumTypeList, GetEnumTypeList method [Windows Properties], GetEnumTypeList method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetEnumTypeList method, IPropertyDescription.GetEnumTypeList, IPropertyDescription::GetEnumTypeList, properties.IPropertyDescription_GetEnumTypeList, propsys/IPropertyDescription::GetEnumTypeList, shell.IPropertyDescription_GetEnumTypeList, shell_IPropertyDescription_GetEnumTypeList
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyDescription::GetEnumTypeList
 - propsys/IPropertyDescription::GetEnumTypeList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription.GetEnumTypeList
---

# IPropertyDescription::GetEnumTypeList


## -description

Gets an instance of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertyenumtypelist">IPropertyEnumTypeList</a>, which can be used to enumerate the possible values for a property.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through ppv, typically IID_IShellItem.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in riid. This is typically [IPropertyEnumTypeList](nn-propsys-ipropertyenumtypelist.md).

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.