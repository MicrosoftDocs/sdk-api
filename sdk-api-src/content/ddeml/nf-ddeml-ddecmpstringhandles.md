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

# DdeCmpStringHandles function


## -description


Compares the values of two string handles. The value of a string handle is not related to the case of the associated string. 


## -parameters




### -param hsz1 [in]

Type: <b>HSZ</b>

A handle to the first string. 


### -param hsz2 [in]

Type: <b>HSZ</b>

A handle to the second string. 


## -returns



Type: <b>int</b>

The return value can be one of the following values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The value of <i>hsz1</i> is either 0 or less than the value of <i>hsz2</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The values of <i>hsz1</i> and <i>hsz2</i> are equal (both can be 0).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The value of <i>hsz2</i> is either 0 or less than the value of <i>hsz1</i>.

</td>
</tr>
</table>
 




## -remarks



An application that must do a case-sensitive comparison of two string handles should compare the string handles directly. An application should use <b>DdeCmpStringHandles</b> for all other comparisons to preserve the case-insensitive nature of Dynamic Data Exchange (DDE). 

<b>DdeCmpStringHandles</b> cannot be used to sort string handles alphabetically. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/7695d435-3bb4-4041-8992-9155efa8911e">DdeAccessData</a>



<a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/93228467-345b-4ff1-942e-2d75a53bce65">DdeFreeStringHandle</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

