---
UID: NF:tom.ITextRange.SetPoint
title: ITextRange::SetPoint (tom.h)
description: Changes the range based on a specified point at or up through (depending on Extend) the point (x, y) aligned according to Type.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","SetPoint method","ITextRange.SetPoint","ITextRange::SetPoint","SetPoint","SetPoint method [Windows Controls]","SetPoint method [Windows Controls]","ITextRange interface","_win32_ITextRange_SetPoint","_win32_ITextRange_SetPoint_cpp","controls.ITextRange_SetPoint","controls._win32_ITextRange_SetPoint","tom/ITextRange::SetPoint"]
old-location: controls\ITextRange_SetPoint.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setpoint.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],SetPoint method, ITextRange.SetPoint, ITextRange::SetPoint, SetPoint, SetPoint method [Windows Controls], SetPoint method [Windows Controls],ITextRange interface, _win32_ITextRange_SetPoint, _win32_ITextRange_SetPoint_cpp, controls.ITextRange_SetPoint, controls._win32_ITextRange_SetPoint, tom/ITextRange::SetPoint
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextRange::SetPoint
 - tom/ITextRange::SetPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange.SetPoint
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

An application can use the specified point in the <a href="/windows/desktop/api/winuser/nf-winuser-windowfrompoint">WindowFromPoint</a> function to get the handle  of the window, which usually can be used to find the client-rectangle coordinates (although a notable exception is with <a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Controls</a>).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-getpoint">GetPoint</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>