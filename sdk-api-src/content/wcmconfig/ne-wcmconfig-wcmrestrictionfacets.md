---
UID: NE:wcmconfig.__MIDL___MIDL_itf_wcmconfig_0000_0000_0005
title: WcmRestrictionFacets (wcmconfig.h)
description: Enumerates the facet values that may be returned by the ISettingsItem::GetRestrictionFacets method.
helpviewer_keywords: ["WcmRestrictionFacets","WcmRestrictionFacets enumeration [SMI]","restrictionFacetEnumeration","restrictionFacetMaxInclusive","restrictionFacetMaxLength","restrictionFacetMinInclusive","smi.wcmrestrictionfacets","wcmconfig/WcmRestrictionFacets","wcmconfig/restrictionFacetEnumeration","wcmconfig/restrictionFacetMaxInclusive","wcmconfig/restrictionFacetMaxLength","wcmconfig/restrictionFacetMinInclusive"]
old-location: smi\wcmrestrictionfacets.htm
tech.root: SMI
ms.assetid: b9e62904-f6a9-4299-a558-51b57bd7d3db
ms.date: 12/05/2018
ms.keywords: WcmRestrictionFacets, WcmRestrictionFacets enumeration [SMI], restrictionFacetEnumeration, restrictionFacetMaxInclusive, restrictionFacetMaxLength, restrictionFacetMinInclusive, smi.wcmrestrictionfacets, wcmconfig/WcmRestrictionFacets, wcmconfig/restrictionFacetEnumeration, wcmconfig/restrictionFacetMaxInclusive, wcmconfig/restrictionFacetMaxLength, wcmconfig/restrictionFacetMinInclusive
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WcmRestrictionFacets
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wcmconfig_0000_0000_0005
 - wcmconfig/__MIDL___MIDL_itf_wcmconfig_0000_0000_0005
 - WcmRestrictionFacets
 - wcmconfig/WcmRestrictionFacets
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcmConfig.h
api_name:
 - WcmRestrictionFacets
---

# WcmRestrictionFacets enumeration


## -description

Enumerates the facet values that may be returned by the <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getrestrictionfacets">ISettingsItem::GetRestrictionFacets</a> method. The facet values are combined by performing an <b>OR</b> operation to provide a full identification of the facets that are defined on the base type for a particular setting. This enumeration type is also used as an input to the <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getrestriction">ISettingsItem::GetRestriction</a> method to specify a facet and retrieve the corresponding information for that facet.

The facet values roughly conform to the  restrictions defined in <a href="/previous-versions/ms256149(v=vs.85)">Data Type Facets</a>. Simple data types (both built-in and derived) have facets. A facet is a single defining aspect that helps determine the set of values for a simple type. For example, <i>MaxLength</i>, <i>minInclusive</i>, and <i>maxInclusive</i> are common facets for the built-in data types. All of the facets for a simple type define the set of legal values for that simple type.

## -enum-fields

### -field restrictionFacetMaxLength:0x1

Maximum number of units of length. Units of length depend on the data type. This value must be a nonNegativeInteger.

### -field restrictionFacetEnumeration:0x2

Specified set of values. This limits a data type to the specified values.

### -field restrictionFacetMaxInclusive:0x4

Maximum value. This value must be the same data type as the inherited data type.

### -field restrictionFacetMinInclusive:0x8

Lower bound value (all values are greater than this value). This value must be the same data type as the inherited data type.
