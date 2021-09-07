---
UID: NF:propsys.IPropertyEnumTypeList.FindMatchingIndex
title: IPropertyEnumTypeList::FindMatchingIndex (propsys.h)
description: Compares the specified property value against the enumerated values in a list and returns the matching index.
helpviewer_keywords: ["FindMatchingIndex","FindMatchingIndex method [Windows Properties]","FindMatchingIndex method [Windows Properties]","IPropertyEnumTypeList interface","IPropertyEnumTypeList interface [Windows Properties]","FindMatchingIndex method","IPropertyEnumTypeList.FindMatchingIndex","IPropertyEnumTypeList::FindMatchingIndex","_shell_IPropertyEnumTypeList_FindMatchingIndex","properties.IPropertyEnumTypeList_FindMatchingIndex","propsys/IPropertyEnumTypeList::FindMatchingIndex","shell.IPropertyEnumTypeList_FindMatchingIndex"]
old-location: properties\IPropertyEnumTypeList_FindMatchingIndex.htm
tech.root: properties
ms.assetid: 48f2d55e-d801-4518-b587-7818cd6afcc9
ms.date: 12/05/2018
ms.keywords: FindMatchingIndex, FindMatchingIndex method [Windows Properties], FindMatchingIndex method [Windows Properties],IPropertyEnumTypeList interface, IPropertyEnumTypeList interface [Windows Properties],FindMatchingIndex method, IPropertyEnumTypeList.FindMatchingIndex, IPropertyEnumTypeList::FindMatchingIndex, _shell_IPropertyEnumTypeList_FindMatchingIndex, properties.IPropertyEnumTypeList_FindMatchingIndex, propsys/IPropertyEnumTypeList::FindMatchingIndex, shell.IPropertyEnumTypeList_FindMatchingIndex
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
 - IPropertyEnumTypeList::FindMatchingIndex
 - propsys/IPropertyEnumTypeList::FindMatchingIndex
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
 - IPropertyEnumTypeList.FindMatchingIndex
---

# IPropertyEnumTypeList::FindMatchingIndex


## -description

Compares the specified property value against the enumerated values in a list and returns the matching index.

## -parameters

### -param propvarCmp [in]

Type: <b>REFPROPVARIANT</b>

A reference to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that represents the property value.

### -param pnIndex [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the index in the enumerated type list that matches the property value, if any.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.