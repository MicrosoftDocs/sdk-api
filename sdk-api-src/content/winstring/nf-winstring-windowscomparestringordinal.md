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

# WindowsCompareStringOrdinal function


## -description


Compares two specified <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> objects and returns an integer that indicates their relative position in a sort order.


## -parameters




### -param string1 [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The first string to compare.


### -param string2 [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The second string to compare.


### -param result [out]

Type: <b>INT32*</b>

A value that indicates the lexical relationship between <i>string1</i> and <i>string2</i>. 


## -returns



Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The  comparison was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>result</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Use the <b>WindowsCompareStringOrdinal</b> function to compare two <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> objects. After the comparison completes, the  <i>result</i> out parameter contains one of three values.


<table>
<tr>
<th>Value</th>
<th>Condition</th>
</tr>
<tr>
<td>-1</td>
<td><i>string1</i> is less than <i>string2</i>.</td>
</tr>
<tr>
<td>0</td>
<td><i>string1</i> equals <i>string2</i>.</td>
</tr>
<tr>
<td>1</td>
<td><i>string1</i> is greater than <i>string2</i>.</td>
</tr>
</table>
 





