---
UID: NE:functiondiscoveryconstraints.tagPropertyConstraint
title: PropertyConstraint (functiondiscoveryconstraints.h)
description: Qualifies the filter conditions used for searching for function instances.
helpviewer_keywords: ["PropertyConstraint","PropertyConstraint enumeration","QC_CONTAINS","QC_DOESNOTEXIST","QC_EQUALS","QC_EXISTS","QC_GREATERTHAN","QC_GREATERTHANOREQUAL","QC_LESSTHAN","QC_LESSTHANOREQUAL","QC_NOTEQUAL","QC_STARTSWITH","functiondiscoveryconstraints/PropertyConstraint","functiondiscoveryconstraints/QC_CONTAINS","functiondiscoveryconstraints/QC_DOESNOTEXIST","functiondiscoveryconstraints/QC_EQUALS","functiondiscoveryconstraints/QC_EXISTS","functiondiscoveryconstraints/QC_GREATERTHAN","functiondiscoveryconstraints/QC_GREATERTHANOREQUAL","functiondiscoveryconstraints/QC_LESSTHAN","functiondiscoveryconstraints/QC_LESSTHANOREQUAL","functiondiscoveryconstraints/QC_NOTEQUAL","functiondiscoveryconstraints/QC_STARTSWITH","ncd.propertyconstraint","tagPropertyConstraint"]
old-location: ncd\propertyconstraint.htm
tech.root: ncd
ms.assetid: 59a3d957-0720-4bd9-b240-512b9cca3c90
ms.date: 12/05/2018
ms.keywords: PropertyConstraint, PropertyConstraint enumeration, QC_CONTAINS, QC_DOESNOTEXIST, QC_EQUALS, QC_EXISTS, QC_GREATERTHAN, QC_GREATERTHANOREQUAL, QC_LESSTHAN, QC_LESSTHANOREQUAL, QC_NOTEQUAL, QC_STARTSWITH, functiondiscoveryconstraints/PropertyConstraint, functiondiscoveryconstraints/QC_CONTAINS, functiondiscoveryconstraints/QC_DOESNOTEXIST, functiondiscoveryconstraints/QC_EQUALS, functiondiscoveryconstraints/QC_EXISTS, functiondiscoveryconstraints/QC_GREATERTHAN, functiondiscoveryconstraints/QC_GREATERTHANOREQUAL, functiondiscoveryconstraints/QC_LESSTHAN, functiondiscoveryconstraints/QC_LESSTHANOREQUAL, functiondiscoveryconstraints/QC_NOTEQUAL, functiondiscoveryconstraints/QC_STARTSWITH, ncd.propertyconstraint, tagPropertyConstraint
req.header: functiondiscoveryconstraints.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PropertyConstraint
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPropertyConstraint
 - functiondiscoveryconstraints/tagPropertyConstraint
 - PropertyConstraint
 - functiondiscoveryconstraints/PropertyConstraint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FunctionDiscoveryConstraints.h
api_name:
 - PropertyConstraint
---

# PropertyConstraint enumeration


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Qualifies the filter conditions used for searching for function instances. This enumeration is used when adding a constraint to a query using the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-addpropertyconstraint">IFunctionInstanceCollectionQuery::AddPropertyConstraint</a> method.

A function instance will only match a property constraint when the property key (PKEY) passed to  <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-addpropertyconstraint">AddPropertyConstraint</a> has the same PROPVARIANT type as the PKEY in the function instance's property store and the PROPVARIANT value satisfies the constraint's filter conditions.

## -enum-fields

### -field QC_EQUALS:0

The constraint's PKEY and the function instance's  PKEY must be equal.

### -field QC_NOTEQUAL:1

The constraint's PKEY and the function instance's  PKEY  must not be equal.

### -field QC_LESSTHAN:2

The constraint's PKEY must be less than the function instance's PKEY. This value can be used only with numbers.

### -field QC_LESSTHANOREQUAL:3

The constraint's PKEY must be less than or equal to the function instance's PKEY. This value can be used only with numbers.

### -field QC_GREATERTHAN:4

The constraint's PKEY must be greater than the function instance's PKEY. This value can be used only with numbers.

### -field QC_GREATERTHANOREQUAL:5

The constraint's PKEY must be greater than or equal to the function instance's PKEY. This value can be used only with numbers.

### -field QC_STARTSWITH:6

The constraint's PKEY must be the start of the function instance's PKEY. This value can be used with strings only.

### -field QC_EXISTS:7

The property must exist.

### -field QC_DOESNOTEXIST:8

The property must not exist.

### -field QC_CONTAINS:9     

The constraint's PKEY value must be contained within the function instance's PKEY value.  This filter is only supported for PROPVARIANTs of type VT_LPWSTR or VT_VECTOR|VT_LPWSTR.

For PROPVARIANTs of type VT_LPWSTR, the constraint PKEY value must be a substring of the function instance's PKEY value.

For PROPVARIANTs of type VT_VECTOR|VT_LPWSTR, the constraint PKEY value must have exactly one element, and matching function instances must have a PKEY with at least one vector element that exactly matches the constraint PKEY value.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-addpropertyconstraint">IFunctionInstanceCollectionQuery::AddPropertyConstraint</a>
