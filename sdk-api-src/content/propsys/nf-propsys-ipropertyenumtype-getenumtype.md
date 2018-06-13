---
UID: NF:propsys.IPropertyEnumType.GetEnumType
title: IPropertyEnumType::GetEnumType
author: windows-sdk-content
description: Gets an enumeration type from an enumeration information structure.
old-location: properties\IPropertyEnumType_GetEnumType.htm
old-project: properties
ms.assetid: f73ad824-5605-4c3c-b623-debdebdf5780
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetEnumType, GetEnumType method [Windows Properties], GetEnumType method [Windows Properties],IPropertyEnumType interface, IPropertyEnumType interface [Windows Properties],GetEnumType method, IPropertyEnumType.GetEnumType, IPropertyEnumType::GetEnumType, PET_DEFAULTVALUE, PET_DISCRETEVALUE, PET_ENDRANGE, PET_RANGEDVALUE, _shell_IPropertyEnumType_GetEnumType, properties.IPropertyEnumType_GetEnumType, propsys/IPropertyEnumType::GetEnumType, shell.IPropertyEnumType_GetEnumType
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
 - IPropertyEnumType.GetEnumType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPropertyEnumType::GetEnumType


## -description


Gets an enumeration type from an enumeration information structure.


## -parameters




### -param penumtype [out]

Type: <b>PROPENUMTYPE*</b>

When this method returns, contains a pointer to one of the values listed below that indicate the enumeration type.



#### PET_DISCRETEVALUE (0)

Use <a href="shell.IPropertyEnumType_GetDisplayText">GetDisplayText</a> and either <a href="shell.IPropertyEnumType_GetRangeMinValue">GetRangeMinValue</a> or <a href="shell.IPropertyEnumType_GetRangeSetValue">GetRangeSetValue</a>.



#### PET_RANGEDVALUE (1)

Use <a href="shell.IPropertyEnumType_GetDisplayText">GetDisplayText</a> and either <a href="shell.IPropertyEnumType_GetRangeMinValue">GetRangeMinValue</a> or <a href="shell.IPropertyEnumType_GetRangeSetValue">GetRangeSetValue</a>.



#### PET_DEFAULTVALUE (2)

Use <a href="shell.IPropertyEnumType_GetDisplayText">GetDisplayText</a>.



#### PET_ENDRANGE (3)

Use <a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a> or <a href="shell.IPropertyEnumType_GetRangeMinValue">GetRangeMinValue</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For additional information, see <a href="shell.propdesc_schema_enumeratedList">enumeratedList</a>.



