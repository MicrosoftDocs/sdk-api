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

# tagPropertyConstraint enumeration


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Qualifies the filter conditions used for searching for function instances. This enumeration is used when adding a constraint to a query using the <a href="https://msdn.microsoft.com/4ff850a8-3208-4fb4-a581-7581e71f34e6">IFunctionInstanceCollectionQuery::AddPropertyConstraint</a> method.

A function instance will only match a property constraint when the property key (PKEY) passed to  <a href="https://msdn.microsoft.com/4ff850a8-3208-4fb4-a581-7581e71f34e6">AddPropertyConstraint</a> has the same PROPVARIANT type as the PKEY in the function instance's property store and the PROPVARIANT value satisfies the constraint's filter conditions.


## -enum-fields




### -field QC_EQUALS

The constraint's PKEY and the function instance's  PKEY must be equal.


### -field QC_NOTEQUAL

The constraint's PKEY and the function instance's  PKEY  must not be equal.


### -field QC_LESSTHAN

The constraint's PKEY must be less than the function instance's PKEY. This value can be used only with numbers.


### -field QC_LESSTHANOREQUAL

The constraint's PKEY must be less than or equal to the function instance's PKEY. This value can be used only with numbers.


### -field QC_GREATERTHAN

The constraint's PKEY must be greater than the function instance's PKEY. This value can be used only with numbers.


### -field QC_GREATERTHANOREQUAL

The constraint's PKEY must be greater than or equal to the function instance's PKEY. This value can be used only with numbers.


### -field QC_STARTSWITH

The constraint's PKEY must be the start of the function instance's PKEY. This value can be used with strings only.


### -field QC_EXISTS

The property must exist.


### -field QC_DOESNOTEXIST

The property must not exist.


### -field QC_CONTAINS

The constraint's PKEY value must be contained within the function instance's PKEY value.  This filter is only supported for PROPVARIANTs of type VT_LPWSTR or VT_VECTOR|VT_LPWSTR.

For PROPVARIANTs of type VT_LPWSTR, the constraint PKEY value must be a substring of the function instance's PKEY value.

For PROPVARIANTs of type VT_VECTOR|VT_LPWSTR, the constraint PKEY value must have exactly one element, and matching function instances must have a PKEY with at least one vector element that exactly matches the constraint PKEY value.


## -see-also




<a href="https://msdn.microsoft.com/4ff850a8-3208-4fb4-a581-7581e71f34e6">IFunctionInstanceCollectionQuery::AddPropertyConstraint</a>
 

 

