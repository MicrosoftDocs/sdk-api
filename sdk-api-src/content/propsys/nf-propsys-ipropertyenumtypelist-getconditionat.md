---
UID: NF:propsys.IPropertyEnumTypeList.GetConditionAt
title: IPropertyEnumTypeList::GetConditionAt (propsys.h)
description: Not supported.Gets the condition at the specified index.
helpviewer_keywords: ["GetConditionAt","GetConditionAt method [Windows Properties]","GetConditionAt method [Windows Properties]","IPropertyEnumTypeList interface","IPropertyEnumTypeList interface [Windows Properties]","GetConditionAt method","IPropertyEnumTypeList.GetConditionAt","IPropertyEnumTypeList::GetConditionAt","_shell_IPropertyEnumTypeList_GetConditionAt","properties.IPropertyEnumTypeList_GetConditionAt","propsys/IPropertyEnumTypeList::GetConditionAt","shell.IPropertyEnumTypeList_GetConditionAt"]
old-location: properties\IPropertyEnumTypeList_GetConditionAt.htm
tech.root: properties
ms.assetid: 0754ac31-09e9-429b-8ae2-58346fb50944
ms.date: 12/05/2018
ms.keywords: GetConditionAt, GetConditionAt method [Windows Properties], GetConditionAt method [Windows Properties],IPropertyEnumTypeList interface, IPropertyEnumTypeList interface [Windows Properties],GetConditionAt method, IPropertyEnumTypeList.GetConditionAt, IPropertyEnumTypeList::GetConditionAt, _shell_IPropertyEnumTypeList_GetConditionAt, properties.IPropertyEnumTypeList_GetConditionAt, propsys/IPropertyEnumTypeList::GetConditionAt, shell.IPropertyEnumTypeList_GetConditionAt
req.header: propsys.h
req.include-header: Propsys.h
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
 - IPropertyEnumTypeList::GetConditionAt
 - propsys/IPropertyEnumTypeList::GetConditionAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - propsys.h
api_name:
 - IPropertyEnumTypeList.GetConditionAt
---

# IPropertyEnumTypeList::GetConditionAt


## -description

Not supported.

Gets the condition at the specified index.

## -parameters

### -param nIndex [in]

Type: <b>UINT</b>

Index of the desired condition.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.