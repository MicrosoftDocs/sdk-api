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

# GetWindowRgnBox function


## -description


The <b>GetWindowRgnBox</b> function retrieves the dimensions of the tightest bounding rectangle for the window region of a window.


## -parameters




### -param hWnd [in]

Handle to the window.


### -param lprc [out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the rectangle dimensions, in device units relative to the upper-left corner of the window.


## -returns



The return value specifies the type of the region that the function obtains. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>COMPLEXREGION</td>
<td>The region is more than one rectangle.</td>
</tr>
<tr>
<td>ERROR</td>
<td>The specified window does not have a region, or an error occurred while attempting to return the region.</td>
</tr>
<tr>
<td>NULLREGION</td>
<td>The region is empty.</td>
</tr>
<tr>
<td>SIMPLEREGION</td>
<td>The region is a single rectangle.</td>
</tr>
</table>
 




## -remarks



The window region determines the area within the window where the system permits drawing. The system does not display any portion of a window that lies outside of the window region. The coordinates of a window's window region are relative to the upper-left corner of the window, not the client area of the window.

To set the window region of a window, call the <a href="https://msdn.microsoft.com/06209d0c-14f9-45ec-ae2c-9cc596b5bbaa">SetWindowRgn</a> function.




## -see-also




<a href="https://msdn.microsoft.com/b4ee68ab-b99e-48b6-90ce-6d6c0ae144e2">GetClipBox</a>



<a href="https://msdn.microsoft.com/c8a8fa46-354b-489e-b016-fd2e728958ce">GetWindowRgn</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/06209d0c-14f9-45ec-ae2c-9cc596b5bbaa">SetWindowRgn</a>
 

 

