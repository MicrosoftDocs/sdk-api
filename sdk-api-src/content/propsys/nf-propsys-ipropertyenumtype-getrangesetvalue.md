---
UID: NF:propsys.IPropertyEnumType.GetRangeSetValue
title: IPropertyEnumType::GetRangeSetValue (propsys.h)
description: Gets a set value from an enumeration information structure.
helpviewer_keywords: ["GetRangeSetValue","GetRangeSetValue method [Windows Properties]","GetRangeSetValue method [Windows Properties]","IPropertyEnumType interface","IPropertyEnumType interface [Windows Properties]","GetRangeSetValue method","IPropertyEnumType.GetRangeSetValue","IPropertyEnumType::GetRangeSetValue","_shell_IPropertyEnumType_GetRangeSetValue","properties.IPropertyEnumType_GetRangeSetValue","propsys/IPropertyEnumType::GetRangeSetValue","shell.IPropertyEnumType_GetRangeSetValue"]
old-location: properties\IPropertyEnumType_GetRangeSetValue.htm
tech.root: properties
ms.assetid: 63c5d2cd-70bc-45f6-a620-7b68ab94f8ff
ms.date: 12/05/2018
ms.keywords: GetRangeSetValue, GetRangeSetValue method [Windows Properties], GetRangeSetValue method [Windows Properties],IPropertyEnumType interface, IPropertyEnumType interface [Windows Properties],GetRangeSetValue method, IPropertyEnumType.GetRangeSetValue, IPropertyEnumType::GetRangeSetValue, _shell_IPropertyEnumType_GetRangeSetValue, properties.IPropertyEnumType_GetRangeSetValue, propsys/IPropertyEnumType::GetRangeSetValue, shell.IPropertyEnumType_GetRangeSetValue
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
 - IPropertyEnumType::GetRangeSetValue
 - propsys/IPropertyEnumType::GetRangeSetValue
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
 - IPropertyEnumType.GetRangeSetValue
---

# IPropertyEnumType::GetRangeSetValue


## -description

Gets a set value from an enumeration information structure.

## -parameters

### -param ppropvarSet [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this method returns, contains a pointer to the set value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For additional information, see <a href="/windows/desktop/properties/propdesc-schema-enumeratedlist">enumeratedList</a>.