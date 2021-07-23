---
UID: NF:propsys.IPropertyEnumTypeList.GetAt
title: IPropertyEnumTypeList::GetAt (propsys.h)
description: Gets the IPropertyEnumType object at the specified index in the list.
helpviewer_keywords: ["GetAt","GetAt method [Windows Properties]","GetAt method [Windows Properties]","IPropertyEnumTypeList interface","IPropertyEnumTypeList interface [Windows Properties]","GetAt method","IPropertyEnumTypeList.GetAt","IPropertyEnumTypeList::GetAt","_shell_IPropertyEnumTypeList_GetAt","properties.IPropertyEnumTypeList_GetAt","propsys/IPropertyEnumTypeList::GetAt","shell.IPropertyEnumTypeList_GetAt"]
old-location: properties\IPropertyEnumTypeList_GetAt.htm
tech.root: properties
ms.assetid: 1713d16f-58d9-46f9-9795-4e05ff257901
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [Windows Properties], GetAt method [Windows Properties],IPropertyEnumTypeList interface, IPropertyEnumTypeList interface [Windows Properties],GetAt method, IPropertyEnumTypeList.GetAt, IPropertyEnumTypeList::GetAt, _shell_IPropertyEnumTypeList_GetAt, properties.IPropertyEnumTypeList_GetAt, propsys/IPropertyEnumTypeList::GetAt, shell.IPropertyEnumTypeList_GetAt
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
 - IPropertyEnumTypeList::GetAt
 - propsys/IPropertyEnumTypeList::GetAt
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
 - IPropertyEnumTypeList.GetAt
---

# IPropertyEnumTypeList::GetAt


## -description

Gets the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertyenumtype">IPropertyEnumType</a> object at the specified index in the list.

## -parameters

### -param itype [in]

Type: <b>UINT</b>

The index of the object in the list.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through ppv, typically IID_IShellItem.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in riid. This is typically [IPropertyEnumType](nn-propsys-ipropertyenumtype.md).

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.