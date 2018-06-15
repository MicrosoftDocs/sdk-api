---
UID: NF:inked.IInkEdit.SetGestureStatus
title: IInkEdit::SetGestureStatus
author: windows-sdk-content
description: Modifies the interest of the InkEdit control in a known application gesture.
old-location: tablet\inkedit_setgesturestatus.htm
old-project: tablet
ms.assetid: 1fc9daa5-ee34-409b-b977-0d39b23d422e
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 1fc9daa5-ee34-409b-b977-0d39b23d422e, IInkEdit interface [Tablet PC],SetGestureStatus method, IInkEdit.SetGestureStatus, IInkEdit::SetGestureStatus, SetGestureStatus, SetGestureStatus method [Tablet PC], SetGestureStatus method [Tablet PC],IInkEdit interface, inked/IInkEdit::SetGestureStatus, tablet.inkedit_setgesturestatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: inked.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SelAlignmentConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkEd.dll
 - InkEd.dll.dll
api_name:
 - IInkEdit.SetGestureStatus
product: Windows
targetos: Windows
req.lib: InkEd.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkEdit::SetGestureStatus


## -description



Modifies the interest of the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control in a known application gesture.




## -parameters




### -param Gesture [in]

The <a href="https://msdn.microsoft.com/87a1db34-371e-4c02-a470-55f35dfbf4ab">IInkGesture</a> object that you want the status of.


### -param Listen [in]

<b>VARIANT_TRUE</b> to indicate that the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control uses the application gesture; otherwise, <b>VARIANT_FALSE</b>.


## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The input parameter was incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_INVALID_MODE</b></dt>
</dl>
</td>
<td width="60%">
InkEdit status must be IES_Idle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
Unsupported gesture.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The flag is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory operation.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/b429ec96-691f-4761-92bf-ef500cf0e1be">IAG_AllGestures</a> gesture is not supported by the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control and returns an error. Passing invalid gesture identifiers does not return an error.

This method should only be called if the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property returns IES_Idle.

To get the interest of the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control in a known gesture, call the <a href="https://msdn.microsoft.com/31973709-1702-4ec1-8228-b0d1bdb64bc8">GetGestureStatus</a> method.




## -see-also




<a href="https://msdn.microsoft.com/736715f4-c610-42cc-9fbb-c2b579da69e5">Gesture Event</a>



<a href="https://msdn.microsoft.com/31973709-1702-4ec1-8228-b0d1bdb64bc8">GetGestureStatus Method [InkEdit Control]</a>



<a href="/windows/desktop/api/inked/nn-inked-iinkedit">IInkEdit</a>



<a href="https://msdn.microsoft.com/b429ec96-691f-4761-92bf-ef500cf0e1be">InkApplicationGesture Enumeration</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

