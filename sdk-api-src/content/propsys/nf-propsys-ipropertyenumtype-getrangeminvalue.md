---
UID: NF:propsys.IPropertyEnumType.GetRangeMinValue
title: IPropertyEnumType::GetRangeMinValue method
author: windows-driver-content
description: Gets a minimum value from an enumeration information structure.
old-location: properties\IPropertyEnumType_GetRangeMinValue.htm
old-project: properties
ms.assetid: e25f776d-f343-4c14-931e-ce2f2761ce2b
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetRangeMinValue method [Windows Properties], GetRangeMinValue method [Windows Properties], IPropertyEnumType interface, GetRangeMinValue,IPropertyEnumType.GetRangeMinValue, IPropertyEnumType, IPropertyEnumType interface [Windows Properties], GetRangeMinValue method, IPropertyEnumType::GetRangeMinValue, _shell_IPropertyEnumType_GetRangeMinValue, properties.IPropertyEnumType_GetRangeMinValue, propsys/IPropertyEnumType::GetRangeMinValue, shell.IPropertyEnumType_GetRangeMinValue
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyEnumType.GetRangeMinValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyEnumType::GetRangeMinValue method


## -description


Gets a minimum value from an enumeration information structure.


## -parameters




### -param ppropvarMin [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this method returns, contains a pointer to the minimum value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For additional information, see <a href="shell.propdesc_schema_enumeratedList">enumeratedList</a>.



