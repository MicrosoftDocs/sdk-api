---
UID: NF:propvarutil.VariantCompare
title: VariantCompare function (propvarutil.h)
description: Compares two variant structures, based on default comparison rules.
helpviewer_keywords: ["VariantCompare","VariantCompare function [Windows Properties]","_shell_VariantCompare","properties.VariantCompare","propvarutil/VariantCompare","shell.VariantCompare"]
old-location: properties\VariantCompare.htm
tech.root: properties
ms.assetid: 45aed78c-1614-4aad-a930-c44615546d6f
ms.date: 12/05/2018
ms.keywords: VariantCompare, VariantCompare function [Windows Properties], _shell_VariantCompare, properties.VariantCompare, propvarutil/VariantCompare, shell.VariantCompare
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - VariantCompare
 - propvarutil/VariantCompare
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantCompare
---

# VariantCompare function


## -description

Compares two variant structures, based on default comparison rules.

## -parameters

### -param var1 [in]

Type: <b>REFVARIANT</b>

Reference to a first variant structure.

### -param var2 [in]

Type: <b>REFVARIANT</b>

Reference to a second variant structure.

## -returns

Type: <b>INT</b>

<ul>
<li>Returns 1 if <i>var1</i> is greater than <i>var2</i></li>
<li>Returns 0 if <i>var1</i> equals <i>var2</i></li>
<li>Returns -1 if <i>var1</i> is less than <i>var2</i></li>
</ul>

## -remarks

<div class="alert"><b>Note</b>  This function does not support the comparison of different VARIANT types. If the types named in <i>var1</i> and <i>var2</i> are different, the results are undefined and should be ignored. Calling applications should ensure that they are comparing two of the same type before they call this function. The <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> function can be used to convert the two structures to the same type.</div>
<div> </div>
By default, VT_NULL / VT_EMPTY / 0-element vectors are considered to be less than any other vartype.