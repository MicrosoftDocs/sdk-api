---
UID: NF:propvarutil.PropVariantCompare
title: PropVariantCompare function
author: windows-sdk-content
description: Compares two PROPVARIANT structures, based on default comparison units and settings.
old-location: properties\PropVariantCompare.htm
tech.root: properties
ms.assetid: f296a583-3af2-4165-8b3a-0b47eba8e89d
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: PropVariantCompare, PropVariantCompare function [Windows Properties], _shell_PropVariantCompare, properties.PropVariantCompare, propvarutil/PropVariantCompare, shell.PropVariantCompare
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - PropVariantCompare
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantCompare function


## -description


Compares two <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures, based on default comparison units and settings.


## -parameters




### -param propvar1 [in]

Type: <b>REFPROPVARIANT</b>

Reference to the first <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param propvar2 [in]

Type: <b>REFPROPVARIANT</b>

Reference to the second <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>INT</b>

<ul>
<li>Returns 1 if <i>propvar1</i> is greater than <i>propvar2</i></li>
<li>Returns 0 if <i>propvar1</i> equals <i>propvar2</i></li>
<li>Returns -1 if <i>propvar1</i> is less than <i>propvar2</i></li>
</ul>



## -remarks



Calling <a href="shell.PropVariantCompare">PropVariantCompare</a> is equivalent to calling <a href="shell.PropVariantCompareEx">PropVariantCompareEx</a> with the PVCHF_DEFAULT flag.

This function compares only selected types, not all types.

By default, VT_NULL / VT_EMPTY / 0-element vectors are considered to be less than any other vartype.

If the vartypes are different, this function attempts to convert <i>propvar2</i> to the vartype of <i>propvar1</i> before comparing them.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.




## -see-also




<a href="shell.PropVariantCompareEx">PropVariantCompareEx</a>
 

 

