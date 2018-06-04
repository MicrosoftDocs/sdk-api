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



<div class="alert"><b>Note</b>  This function does not support the comparison of different VARIANT types. If the types named in <i>var1</i> and <i>var2</i> are different, the results are undefined and should be ignored. Calling applications should ensure that they are comparing two of the same type before they call this function. The <a href="shell.PropVariantChangeType">PropVariantChangeType</a> function can be used to convert the two structures to the same type.</div>
<div> </div>
By default, VT_NULL / VT_EMPTY / 0-element vectors are considered to be less than any other vartype.



