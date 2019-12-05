---
UID: NF:propsys.IPropertyEnumType.GetValue
title: IPropertyEnumType::GetValue (propsys.h)
description: Gets a value from an enumeration information structure.
old-location: properties\IPropertyEnumType_GetValue.htm
tech.root: properties
ms.assetid: e820087b-95fb-4352-9bb0-cf34216d37a6
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Windows Properties], GetValue method [Windows Properties],IPropertyEnumType interface, IPropertyEnumType interface [Windows Properties],GetValue method, IPropertyEnumType.GetValue, IPropertyEnumType::GetValue, _shell_IPropertyEnumType_GetValue, properties.IPropertyEnumType_GetValue, propsys/IPropertyEnumType::GetValue, shell.IPropertyEnumType_GetValue
ms.topic: method
f1_keywords:
- propsys/IPropertyEnumType.GetValue
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Propsys.h
api_name:
- IPropertyEnumType.GetValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyEnumType::GetValue


## -description


Gets a value from an enumeration information structure.


## -parameters




### -param ppropvar [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this method returns, contains a pointer to the property value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For additional information, see <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-enumeratedlist">enumeratedList</a>.



