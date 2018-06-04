---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



