---
UID: NF:propsys.IPropertyDescription.GetGroupingRange
title: IPropertyDescription::GetGroupingRange method
author: windows-driver-content
description: Gets the grouping method to be used when a view is grouped by a property, and retrieves the grouping type.
old-location: properties\IPropertyDescription_GetGroupingRange.htm
old-project: properties
ms.assetid: 9533c43f-1b51-4aa0-9579-0a3053102b24
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetGroupingRange method [Windows Properties], GetGroupingRange method [Windows Properties], IPropertyDescription interface, GetGroupingRange,IPropertyDescription.GetGroupingRange, IPropertyDescription, IPropertyDescription interface [Windows Properties], GetGroupingRange method, IPropertyDescription::GetGroupingRange, PDGR_ALPHANUMERIC, PDGR_DATE, PDGR_DISCRETE, PDGR_DYNAMIC, PDGR_ENUMERATED, PDGR_PERCENT, PDGR_SIZE, properties.IPropertyDescription_GetGroupingRange, propsys/IPropertyDescription::GetGroupingRange, shell.IPropertyDescription_GetGroupingRange, shell_IPropertyDescription_GetGroupingRange
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
-	IPropertyDescription.GetGroupingRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyDescription::GetGroupingRange method


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
 

 

