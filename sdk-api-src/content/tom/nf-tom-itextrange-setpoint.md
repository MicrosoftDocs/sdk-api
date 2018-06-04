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

# ITextRange::SetPoint


## -description


Changes the range based on a specified point at or up through (depending on <i>Extend</i>) the point (<i>x</i>, <i>y</i>) aligned according to <i>Type</i>. 


## -parameters




### -param x [in]

Type: <b>long</b>

Horizontal coordinate of the specified point, in absolute screen coordinates. 


### -param y [in]

Type: <b>long</b>

Vertical coordinate of the specified point, in absolute screen coordinates. 


### -param Type [in]

Type: <b>long</b>

The end to move to the specified point. It can be one of the following. 
					

<table class="clsStd">
<tr>
<td><b>tomStart</b></td>
<td>Move the start of range.</td>
</tr>
<tr>
<td><b>tomEnd</b></td>
<td>Move the end of range.</td>
</tr>
</table>
 


### -param Extend [in]

Type: <b>long</b>

How to set the endpoints of the range. If <i>Extend</i> is zero (the default), the range is an insertion point at the specified point (or at the nearest point with selectable text). If <i>Extend</i> is 1, the end specified by <i>Type</i> is moved to the point and the other end is left alone. 


## -returns



Type: <b>HRESULT</b>

The method returns <b>S_OK</b>.




## -remarks



An application can use the specified point in the <a href="https://msdn.microsoft.com/e4830394-f994-4d29-b843-3a618e331d52">WindowFromPoint</a> function to get the handle  of the window, which usually can be used to find the client-rectangle coordinates (although a notable exception is with <a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Controls</a>).




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/67bb38d8-d96d-4d17-876d-4cadc39adece">GetPoint</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

