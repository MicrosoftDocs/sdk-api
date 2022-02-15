---
UID: NF:propsys.IPropertyDescription.GetGroupingRange
title: IPropertyDescription::GetGroupingRange (propsys.h)
description: Gets the grouping method to be used when a view is grouped by a property, and retrieves the grouping type.
old-location: properties\IPropertyDescription_GetGroupingRange.htm
tech.root: properties
ms.assetid: 9533c43f-1b51-4aa0-9579-0a3053102b24
ms.date: 12/05/2018
ms.keywords: GetGroupingRange, GetGroupingRange method [Windows Properties], GetGroupingRange method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetGroupingRange method, IPropertyDescription.GetGroupingRange, IPropertyDescription::GetGroupingRange, PDGR_ALPHANUMERIC, PDGR_DATE, PDGR_DISCRETE, PDGR_DYNAMIC, PDGR_ENUMERATED, PDGR_PERCENT, PDGR_SIZE, properties.IPropertyDescription_GetGroupingRange, propsys/IPropertyDescription::GetGroupingRange, shell.IPropertyDescription_GetGroupingRange, shell_IPropertyDescription_GetGroupingRange
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
 - IPropertyDescription::GetGroupingRange
 - propsys/IPropertyDescription::GetGroupingRange
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
 - IPropertyDescription.GetGroupingRange
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

Displays percent groups returned by <a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescription-getenumtypelist">IPropertyDescription::GetEnumTypeList</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The information retrieved by this method comes from the <i>groupingRange</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>