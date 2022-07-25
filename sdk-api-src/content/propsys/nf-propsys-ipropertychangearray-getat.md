---
UID: NF:propsys.IPropertyChangeArray.GetAt
title: IPropertyChangeArray::GetAt (propsys.h)
description: Gets the change operation at a specified array index.
helpviewer_keywords: ["GetAt","GetAt method [Windows Properties]","GetAt method [Windows Properties]","IPropertyChangeArray interface","IPropertyChangeArray interface [Windows Properties]","GetAt method","IPropertyChangeArray.GetAt","IPropertyChangeArray::GetAt","_shell_IPropertyChangeArray_GetAt","properties.IPropertyChangeArray_GetAt","propsys/IPropertyChangeArray::GetAt","shell.IPropertyChangeArray_GetAt"]
old-location: properties\IPropertyChangeArray_GetAt.htm
tech.root: properties
ms.assetid: bc20e4a3-1405-494a-98ea-cca4c87e4984
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [Windows Properties], GetAt method [Windows Properties],IPropertyChangeArray interface, IPropertyChangeArray interface [Windows Properties],GetAt method, IPropertyChangeArray.GetAt, IPropertyChangeArray::GetAt, _shell_IPropertyChangeArray_GetAt, properties.IPropertyChangeArray_GetAt, propsys/IPropertyChangeArray::GetAt, shell.IPropertyChangeArray_GetAt
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
 - IPropertyChangeArray::GetAt
 - propsys/IPropertyChangeArray::GetAt
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
 - IPropertyChangeArray.GetAt
---

# IPropertyChangeArray::GetAt


## -description

Gets the change operation at a specified array index.

## -parameters

### -param iIndex [in]

Type: <b>UINT</b>

The index of the change to retrieve.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired IID.

### -param ppv [out]

Type: <b>void**</b>

The address of a pointer to the interface specified by <i>riid</i>, usually <a href="/windows/desktop/api/propsys/nn-propsys-ipropertychange">IPropertyChange</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.