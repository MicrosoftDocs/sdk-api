---
UID: NF:tom.ITextRange.SetPoint
title: ITextRange::SetPoint
author: windows-driver-content
description: Changes the range based on a specified point at or up through (depending on Extend) the point (x, y) aligned according to Type.
old-location: controls\ITextRange_SetPoint.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setpoint.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: ITextRange interface [Windows Controls],SetPoint method, ITextRange.SetPoint, ITextRange::SetPoint, SetPoint, SetPoint method [Windows Controls], SetPoint method [Windows Controls],ITextRange interface, _win32_ITextRange_SetPoint, _win32_ITextRange_SetPoint_cpp, controls.ITextRange_SetPoint, controls._win32_ITextRange_SetPoint, tom/ITextRange::SetPoint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextRange.SetPoint
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

