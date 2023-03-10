---
UID: NF:propsys.IPropertyChangeArray.IsKeyInArray
title: IPropertyChangeArray::IsKeyInArray (propsys.h)
description: Specifies whether a particular property key exists in the change array.
helpviewer_keywords: ["IPropertyChangeArray interface [Windows Properties]","IsKeyInArray method","IPropertyChangeArray.IsKeyInArray","IPropertyChangeArray::IsKeyInArray","IsKeyInArray","IsKeyInArray method [Windows Properties]","IsKeyInArray method [Windows Properties]","IPropertyChangeArray interface","_shell_IPropertyChangeArray_IsKeyInArray","properties.IPropertyChangeArray_IsKeyInArray","propsys/IPropertyChangeArray::IsKeyInArray","shell.IPropertyChangeArray_IsKeyInArray"]
old-location: properties\IPropertyChangeArray_IsKeyInArray.htm
tech.root: properties
ms.assetid: aa6fe869-6fb7-4d2e-8dd8-65da0cbcd7bc
ms.date: 12/05/2018
ms.keywords: IPropertyChangeArray interface [Windows Properties],IsKeyInArray method, IPropertyChangeArray.IsKeyInArray, IPropertyChangeArray::IsKeyInArray, IsKeyInArray, IsKeyInArray method [Windows Properties], IsKeyInArray method [Windows Properties],IPropertyChangeArray interface, _shell_IPropertyChangeArray_IsKeyInArray, properties.IPropertyChangeArray_IsKeyInArray, propsys/IPropertyChangeArray::IsKeyInArray, shell.IPropertyChangeArray_IsKeyInArray
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
 - IPropertyChangeArray::IsKeyInArray
 - propsys/IPropertyChangeArray::IsKeyInArray
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
 - IPropertyChangeArray.IsKeyInArray
---

# IPropertyChangeArray::IsKeyInArray


## -description

Specifies whether a particular property key exists in the change array.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure of interest.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if key is found; otherwise, E_FAIL.