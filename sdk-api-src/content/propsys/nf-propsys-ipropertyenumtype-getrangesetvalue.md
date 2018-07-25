---
UID: NF:propsys.IPropertyEnumType.GetRangeSetValue
title: IPropertyEnumType::GetRangeSetValue
author: windows-sdk-content
description: Gets a set value from an enumeration information structure.
old-location: properties\IPropertyEnumType_GetRangeSetValue.htm
old-project: properties
ms.assetid: 63c5d2cd-70bc-45f6-a620-7b68ab94f8ff
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetRangeSetValue, GetRangeSetValue method [Windows Properties], GetRangeSetValue method [Windows Properties],IPropertyEnumType interface, IPropertyEnumType interface [Windows Properties],GetRangeSetValue method, IPropertyEnumType.GetRangeSetValue, IPropertyEnumType::GetRangeSetValue, _shell_IPropertyEnumType_GetRangeSetValue, properties.IPropertyEnumType_GetRangeSetValue, propsys/IPropertyEnumType::GetRangeSetValue, shell.IPropertyEnumType_GetRangeSetValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyEnumType.GetRangeSetValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyEnumType::GetRangeSetValue


## -description


Gets a set value from an enumeration information structure.


## -parameters




### -param ppropvarSet [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this method returns, contains a pointer to the set value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For additional information, see <a href="shell.propdesc_schema_enumeratedList">enumeratedList</a>.



