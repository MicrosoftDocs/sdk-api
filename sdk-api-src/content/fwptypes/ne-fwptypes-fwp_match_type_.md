---
UID: NE:fwptypes.FWP_MATCH_TYPE_
title: FWP_MATCH_TYPE_
author: windows-sdk-content
description: The FWP_MATCH_TYPE enumeration type specifies the type of match that a filter should use to test for a particular condition.
old-location: netvista\fwp_match_type.htm
tech.root: NetVista
ms.assetid: c0f95b3f-1b89-4d44-87b2-73032fa3524e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWP_MATCH_EQUAL, FWP_MATCH_EQUAL_CASE_INSENSITIVE, FWP_MATCH_FLAGS_ALL_SET, FWP_MATCH_FLAGS_ANY_SET, FWP_MATCH_FLAGS_NONE_SET, FWP_MATCH_GREATER, FWP_MATCH_GREATER_OR_EQUAL, FWP_MATCH_LESS, FWP_MATCH_LESS_OR_EQUAL, FWP_MATCH_NOT_EQUAL, FWP_MATCH_RANGE, FWP_MATCH_TYPE, FWP_MATCH_TYPE enumeration [Network Drivers Starting with Windows Vista], FWP_MATCH_TYPE_, FWP_MATCH_TYPE_MAX, fwptypes/FWP_MATCH_EQUAL, fwptypes/FWP_MATCH_EQUAL_CASE_INSENSITIVE, fwptypes/FWP_MATCH_FLAGS_ALL_SET, fwptypes/FWP_MATCH_FLAGS_ANY_SET, fwptypes/FWP_MATCH_FLAGS_NONE_SET, fwptypes/FWP_MATCH_GREATER, fwptypes/FWP_MATCH_GREATER_OR_EQUAL, fwptypes/FWP_MATCH_LESS, fwptypes/FWP_MATCH_LESS_OR_EQUAL, fwptypes/FWP_MATCH_NOT_EQUAL, fwptypes/FWP_MATCH_RANGE, fwptypes/FWP_MATCH_TYPE, fwptypes/FWP_MATCH_TYPE_MAX, netvista.fwp_match_type, wfp_ref_4_enum_81a997f9-e9a8-43a7-82a0-6571c7a12b3a.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fwptypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with  Windows Vista.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwptypes.h
api_name:
 - FWP_MATCH_TYPE
product: Windows
targetos: Windows
req.typenames: FWP_MATCH_TYPE
req.redist: 
---

# FWP_MATCH_TYPE_ enumeration


## -description


The FWP_MATCH_TYPE enumeration type specifies the type of match that a filter should use to test for
  a particular condition.


## -enum-fields




### -field FWP_MATCH_EQUAL

Tests whether the value is equal to the condition value.


### -field FWP_MATCH_GREATER

Tests whether the value is greater than the condition value.


### -field FWP_MATCH_LESS

Tests whether the value is less than the condition value.


### -field FWP_MATCH_GREATER_OR_EQUAL

Tests whether the value is greater than or equal to the condition value.


### -field FWP_MATCH_LESS_OR_EQUAL

Tests whether the value is less than or equal to the condition value.


### -field FWP_MATCH_RANGE

Tests whether the value is within a given range of condition values.


### -field FWP_MATCH_FLAGS_ALL_SET

Tests whether all of the condition flags specified in the condition value are set.


### -field FWP_MATCH_FLAGS_ANY_SET

Tests whether any of the condition flags specified in the condition value are set.


### -field FWP_MATCH_FLAGS_NONE_SET

Tests whether none of the condition flags specified in the condition value are set.


### -field FWP_MATCH_EQUAL_CASE_INSENSITIVE

Tests whether the string of Unicode characters is the same as the condition value string. This test
     considers uppercase and lowercase characters to be equal.


### -field FWP_MATCH_NOT_EQUAL

Tests whether the value is not equal to the condition value.


### -field FWP_MATCH_PREFIX


### -field FWP_MATCH_NOT_PREFIX


### -field FWP_MATCH_TYPE_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.


## -remarks



The 
    <a href="https://msdn.microsoft.com/d4a20939-4866-4402-9b29-d94c2170807c">FWPS_FILTER_CONDITION0</a> structure
    contains a member of type FWP_MATCH_TYPE that specifies the type of match that the filter should use to
    test whether that particular condition is true.




## -see-also




<a href="https://msdn.microsoft.com/d4a20939-4866-4402-9b29-d94c2170807c">FWPS_FILTER_CONDITION0</a>
 

 

