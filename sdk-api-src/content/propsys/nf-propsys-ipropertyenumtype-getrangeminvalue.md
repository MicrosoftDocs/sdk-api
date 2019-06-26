---
UID: NF:propsys.IPropertyEnumType.GetRangeMinValue
title: IPropertyEnumType::GetRangeMinValue (propsys.h)
author: windows-sdk-content
description: Gets a minimum value from an enumeration information structure.
old-location: properties\IPropertyEnumType_GetRangeMinValue.htm
tech.root: properties
ms.assetid: e25f776d-f343-4c14-931e-ce2f2761ce2b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRangeMinValue, GetRangeMinValue method [Windows Properties], GetRangeMinValue method [Windows Properties],IPropertyEnumType interface, IPropertyEnumType interface [Windows Properties],GetRangeMinValue method, IPropertyEnumType.GetRangeMinValue, IPropertyEnumType::GetRangeMinValue, _shell_IPropertyEnumType_GetRangeMinValue, properties.IPropertyEnumType_GetRangeMinValue, propsys/IPropertyEnumType::GetRangeMinValue, shell.IPropertyEnumType_GetRangeMinValue
ms.topic: method
f1_keywords: 
 - "propsys/IPropertyEnumType.GetRangeMinValue"
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
 - IPropertyEnumType.GetRangeMinValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyEnumType::GetRangeMinValue


## -description


Gets a minimum value from an enumeration information structure.


## -parameters




### -param ppropvarMin [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a>*</b>

When this method returns, contains a pointer to the minimum value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For additional information, see <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-enumeratedlist">enumeratedList</a>.



