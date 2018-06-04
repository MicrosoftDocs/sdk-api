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

# IPropertyDescription::GetGroupingRange


## -description


Gets the grouping method to be used when a view is grouped by a property, and retrieves the grouping type.


## -parameters




### -param pgr [out]

Type: <b>PROPDESC_GROUPING_RANGE*</b>

Receives a pointer to a flag value that indicates the grouping type. The possible values are:



#### PDGR_DISCRETE

Displays individual values.



#### PDGR_ALPHANUMERIC

Displays static alphanumeric ranges.



#### PDGR_SIZE

Displays static size ranges.



#### PDGR_DYNAMIC

Displays dynamically created ranges.



#### PDGR_DATE

Displays month and year groups.



#### PDGR_PERCENT

Displays percent groups.



#### PDGR_ENUMERATED

Displays percent groups returned by <a href="shell.IPropertyDescription_GetEnumTypeList">IPropertyDescription::GetEnumTypeList</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The information retrieved by this method comes from the <i>groupingRange</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

