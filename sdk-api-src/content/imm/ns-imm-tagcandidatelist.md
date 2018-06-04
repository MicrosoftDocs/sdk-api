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

# tagCANDIDATELIST structure


## -description



Contains information about a candidate list.




## -struct-fields




### -field dwSize

Size, in bytes, of the structure, the offset array, and all candidate strings.


### -field dwStyle

Candidate style values. This member can have one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>IME_CAND_UNKNOWN</td>
<td>Candidates are in a style other than listed here.</td>
</tr>
<tr>
<td>IME_CAND_READ</td>
<td>Candidates are in same reading.</td>
</tr>
<tr>
<td>IME_CAND_CODE</td>
<td>Candidates are in a code range.</td>
</tr>
<tr>
<td>IME_CAND_MEANING</td>
<td>Candidates are in same meaning.</td>
</tr>
<tr>
<td>IME_CAND_RADICAL</td>
<td>Candidates use same radical character.</td>
</tr>
<tr>
<td>IME_CAND_STROKES</td>
<td>Candidates are in same number of strokes.</td>
</tr>
</table>
 

For the IME_CAND_CODE style, the candidate list has a special structure depending on the value of the <b>dwCount</b> member. If <b>dwCount</b> is 1, the <b>dwOffset</b> member contains a single DBCS character rather than an offset, and no candidate string is provided. If the <b>dwCount</b> member is greater than 1, the <b>dwOffset</b> member contains valid offsets, and the candidate strings are text representations of individual DBCS character values in hexadecimal notation.


### -field dwCount

Number of candidate strings.


### -field dwSelection

Index of the selected candidate string.


### -field dwPageStart

Index of the first candidate string in the candidate window. This varies as the user presses the PAGE UP and PAGE DOWN keys.


### -field dwPageSize

Number of candidate strings to be shown in one page in the candidate window. The user can move to the next page by pressing IME-defined keys, such as the PAGE UP or PAGE DOWN key. If this number is 0, an application can define a proper value by itself.


### -field dwOffset

Offset to the start of the first candidate string, relative to the start of this structure. The offsets for subsequent strings immediately follow this member, forming an array of 32-bit offsets.


## -remarks



The candidate strings immediately follow the last offset in the <b>dwOffset</b> array.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/1be3ae8b-e083-4420-bc8a-7f49c4264cab">Input Method Manager Structures</a>
 

 

