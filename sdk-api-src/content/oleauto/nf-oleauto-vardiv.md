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

# VarDiv function


## -description


Returns the result from dividing two variants.




## -parameters




### -param pvarLeft [in]

The first variant.


### -param pvarRight [in]

The second variant.


### -param pvarResult [out]

The result variant.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The function operates as follows.

<table>
<tr>
<th>Condition</th>
<th>Result</th>
</tr>
<tr>
<td>Both expressions are strings, dates, characters, or boolean values</td>
<td>Double</td>
</tr>
<tr>
<td>One expression is a string and the other a character</td>
<td>Division and a double is returned</td>
</tr>
<tr>
<td>One expression is numeric and the other a string</td>
<td>Division and a double is returned</td>
</tr>
<tr>
<td>Both expressions are numeric</td>
<td>Division and a double is returned</td>
</tr>
<tr>
<td>Either expression is null</td>
<td>Null</td>
</tr>
<tr>
<td><i>pvarRight</i> is empty and <i>pvarLeft</i> is not empty</td>
<td>DISP_E_DIVBYZERO</td>
</tr>
<tr>
<td><i>pvarLeft</i> is empty and <i>pvarRight</i> is not empty</td>
<td>0 as type double</td>
</tr>
<tr>
<td>Both expressions are empty</td>
<td>DISP_E_OVERFLOW</td>
</tr>
</table>
 



