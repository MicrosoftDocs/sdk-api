---
UID: NF:dcomptypes.tagCOMPOSITION_TARGET_ID.operator-equal-equal-to
tech.root: directcomp
title: tagCOMPOSITION_TARGET_ID::operator==
ms.date: 06/24/2021
targetos: Windows
description: Compares the values of two `COMPOSITION_TARGET_ID` objects to see if they contain identical values.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: dcomptypes.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dcomptypes.h
api_name:
 - tagCOMPOSITION_TARGET_ID::operator==
f1_keywords:
 - tagCOMPOSITION_TARGET_ID::operator==
 - dcomptypes/tagCOMPOSITION_TARGET_ID::operator==
dev_langs:
 - c++
---

## -description

Compares the values of two `COMPOSITION_TARGET_ID` objects to see if they contain identical values.

## -parameters

### -param rhs

A reference to the `COMPOSITION_TARGET_ID` object that is compared to this one.

## -returns

`TRUE` if this composition target ID and the composition target ID specified by _rhs_ contain identical values; otherwise, `FALSE`.

## -remarks

The `COMPOSITION_TARGET_ID` comparison operators (== != &lt; &lt;= &gt; &gt;=) have been overloaded to compare the values of two `COMPOSITION_TARGET_ID` objects.

The `uniqueId` value is considered to be the same if either `COMPOSITION_TARGET_ID` has a `uniqueID` of 0.

## -see-also

