---
UID: NF:propsys.IPropertyDescription.GetAggregationType
title: IPropertyDescription::GetAggregationType (propsys.h)
description: Gets a value that describes how the property values are displayed when multiple items are selected in the UI.
old-location: properties\IPropertyDescription_GetAggregationType.htm
tech.root: properties
ms.assetid: d8507f19-1778-42b1-bd40-12fec45cd03e
ms.date: 12/05/2018
ms.keywords: GetAggregationType, GetAggregationType method [Windows Properties], GetAggregationType method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetAggregationType method, IPropertyDescription.GetAggregationType, IPropertyDescription::GetAggregationType, properties.IPropertyDescription_GetAggregationType, propsys/IPropertyDescription::GetAggregationType, shell.IPropertyDescription_GetAggregationType, shell_IPropertyDescription_GetAggregationType
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
 - IPropertyDescription::GetAggregationType
 - propsys/IPropertyDescription::GetAggregationType
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
 - IPropertyDescription.GetAggregationType
---

# IPropertyDescription::GetAggregationType


## -description

Gets a value that describes how the property values are displayed when multiple items are selected in the UI.

## -parameters

### -param paggtype [out]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-propdesc_aggregation_type">PROPDESC_AGGREGATION_TYPE</a>*</b>

When this method returns, contains a pointer to a value that indicates the aggregation type. See <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_aggregation_type">PROPDESC_AGGREGATION_TYPE</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The information retrieved by this method comes from the <i>aggregationType</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>