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

# tagCOMPOSITIONFORM structure


## -description



Contains style and position information for a composition window.




## -struct-fields




### -field dwStyle

Position style. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>CFS_DEFAULT</td>
<td>Move the composition window to the default position. The IME window can display the composition window outside the client area, such as in a floating window.</td>
</tr>
<tr>
<td>CFS_FORCE_POSITION</td>
<td>Display the upper left corner of the composition window at exactly the position specified by <b>ptCurrentPos</b>. The coordinates are relative to the upper left corner of the window containing the composition window and are not subject to adjustment by the IME.</td>
</tr>
<tr>
<td>CFS_POINT</td>
<td>Display the upper left corner of the composition window at the position specified by <b>ptCurrentPos</b>. The coordinates are relative to the upper left corner of the window containing the composition window and are subject to adjustment by the IME.</td>
</tr>
<tr>
<td>CFS_RECT</td>
<td>Display the composition window at the position specified by <b>rcArea</b>. The coordinates are relative to the upper left of the window containing the composition window.</td>
</tr>
</table>
 


### -field ptCurrentPos

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure containing the coordinates of the upper left corner of the composition window.


### -field rcArea

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the coordinates of the upper left and lower right corners of the composition window.


## -remarks



Some IME windows adjust the composition window position specified by the system or the application. The CFS_FORCE_POSITION directs the IME window to skip this adjustment.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/1be3ae8b-e083-4420-bc8a-7f49c4264cab">Input Method Manager Structures</a>
 

 

