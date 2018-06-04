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

# tagCANDIDATEFORM structure


## -description



Contains position information for the candidate window.




## -struct-fields




### -field dwIndex

Candidate list identifier. It is 0 for the first list, 1 for the second, and so on. The maximum index is 3.


### -field dwStyle

Position style. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>CFS_CANDIDATEPOS</td>
<td>Display the upper left corner of the candidate list window at the position specified by <b>ptCurrentPos</b>. The coordinates are relative to the upper left corner of the window containing the list window, and are subject to adjustment by the system.</td>
</tr>
<tr>
<td>CFS_EXCLUDE</td>
<td>Exclude the candidate window from the area specified by <b>rcArea</b>. The <b>ptCurrentPos</b> member specifies the coordinates of the current point of interest, typically the caret position.</td>
</tr>
</table>
 


### -field ptCurrentPos

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure containing the coordinates of the upper left corner of the candidate window or the caret position, depending on the value of <b>dwStyle</b>.


### -field rcArea

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the coordinates of the upper left and lower right corners of the exclusion area.


## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/1be3ae8b-e083-4420-bc8a-7f49c4264cab">Input Method Manager Structures</a>
 

 

