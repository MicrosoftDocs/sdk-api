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

# VarR4CmpR8 function


## -description


Compares two variants of types float and double.


## -parameters




### -param fltLeft [in]

The first variant.


### -param dblRight [in]

The second variant.


## -returns



The function returns the following as a SUCCESS HRESULT.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b></b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
<i>fltLeft</i> is less than <i>dblRight.</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b></b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The two parameters are equal.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b></b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
<i>fltLeft</i> is greater than <i>dblRight.</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b></b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Either expression is NULL.


</td>
</tr>
</table>
 



