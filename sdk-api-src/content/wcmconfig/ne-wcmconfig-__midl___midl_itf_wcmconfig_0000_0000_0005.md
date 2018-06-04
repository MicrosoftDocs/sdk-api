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

# __MIDL___MIDL_itf_wcmconfig_0000_0000_0005 enumeration


## -description


Enumerates the facet values that may be returned by the <a href="https://msdn.microsoft.com/64cf82d5-c210-4ff2-a7c8-1a284859382e">ISettingsItem::GetRestrictionFacets</a> method. The facet values are combined by performing an <b>OR</b> operation to provide a full identification of the facets that are defined on the base type for a particular setting. This enumeration type is also used as an input to the <a href="https://msdn.microsoft.com/14bc4956-e8ea-464b-949e-ddc7ae445c1a">ISettingsItem::GetRestriction</a> method to specify a facet and retrieve the corresponding information for that facet.

The facet values roughly conform to the  restrictions defined in <a href="88c691a0-a38e-4025-9f39-bcd2a4447f1b">Data Type Facets</a>. Simple data types (both built-in and derived) have facets. A facet is a single defining aspect that helps determine the set of values for a simple type. For example, <i>MaxLength</i>, <i>minInclusive</i>, and <i>maxInclusive</i> are common facets for the built-in data types. All of the facets for a simple type define the set of legal values for that simple type.


## -enum-fields




### -field restrictionFacetMaxLength

Maximum number of units of length. Units of length depend on the data type. This value must be a nonNegativeInteger.


### -field restrictionFacetEnumeration

Specified set of values. This limits a data type to the specified values.


### -field restrictionFacetMaxInclusive

Maximum value. This value must be the same data type as the inherited data type.


### -field restrictionFacetMinInclusive

Lower bound value (all values are greater than this value). This value must be the same data type as the inherited data type.

