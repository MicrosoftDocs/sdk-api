---
UID: NF:propvarutil.PropVariantCompare
title: PropVariantCompare function (propvarutil.h)
description: Compares two PROPVARIANT structures, based on default comparison units and settings.
helpviewer_keywords: ["PropVariantCompare","PropVariantCompare function [Windows Properties]","_shell_PropVariantCompare","properties.PropVariantCompare","propvarutil/PropVariantCompare","shell.PropVariantCompare"]
old-location: properties\PropVariantCompare.htm
tech.root: properties
ms.assetid: f296a583-3af2-4165-8b3a-0b47eba8e89d
ms.date: 12/05/2018
ms.keywords: PropVariantCompare, PropVariantCompare function [Windows Properties], _shell_PropVariantCompare, properties.PropVariantCompare, propvarutil/PropVariantCompare, shell.PropVariantCompare
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PropVariantCompare
 - propvarutil/PropVariantCompare
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - PropVariantCompare
---

# PropVariantCompare function


## -description

Compares two <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures, based on default comparison units and settings.

## -parameters

### -param propvar1 [in]

Type: <b>REFPROPVARIANT</b>

Reference to the first <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param propvar2 [in]

Type: <b>REFPROPVARIANT</b>

Reference to the second <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>INT</b>

<ul>
<li>Returns 1 if <i>propvar1</i> is greater than <i>propvar2</i></li>
<li>Returns 0 if <i>propvar1</i> equals <i>propvar2</i></li>
<li>Returns -1 if <i>propvar1</i> is less than <i>propvar2</i></li>
</ul>

## -remarks

Calling <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantcompare">PropVariantCompare</a> is equivalent to calling <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantcompareex">PropVariantCompareEx</a> with the PVCHF_DEFAULT flag.

This function compares only selected types, not all types.

By default, VT_NULL / VT_EMPTY / 0-element vectors are considered to be less than any other vartype.

If the vartypes are different, this function attempts to convert <i>propvar2</i> to the vartype of <i>propvar1</i> before comparing them.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantcompareex">PropVariantCompareEx</a>