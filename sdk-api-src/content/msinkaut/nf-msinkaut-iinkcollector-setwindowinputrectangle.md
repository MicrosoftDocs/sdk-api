---
UID: NF:msinkaut.IInkCollector.SetWindowInputRectangle
title: IInkCollector::SetWindowInputRectangle
author: windows-sdk-content
description: Sets the window rectangle, in pixels, within which ink is drawn.
old-location: tablet\inkcollector_setwindowinputrectangle.htm
old-project: tablet
ms.assetid: b46139db-0473-4cd3-8f1b-d303f3430470
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: IInkCollector interface [Tablet PC],SetWindowInputRectangle method, IInkCollector.SetWindowInputRectangle, IInkCollector::SetWindowInputRectangle, SetWindowInputRectangle, SetWindowInputRectangle method [Tablet PC], SetWindowInputRectangle method [Tablet PC],IInkCollector interface, b46139db-0473-4cd3-8f1b-d303f3430470, msinkaut/IInkCollector::SetWindowInputRectangle, tablet.inkcollector_setwindowinputrectangle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkCollector.SetWindowInputRectangle
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkCollector::SetWindowInputRectangle


## -description



Sets the window rectangle, in pixels, within which ink is drawn.




## -parameters




### -param WindowInputRectangle [in]

The rectangle, in window coordinates, on which ink is drawn.


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
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The rectangle coordinates are invalid (for example, width/height of 0).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_COLLECTOR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
Cannot update mappings while in the middle of a stroke.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_OVERLAPPING_INPUT_RECT</b></dt>
</dl>
</td>
<td width="60%">
The window input rectangle overlaps with the window input rectangle of an enabled InkCollector.

</td>
</tr>
</table>
 




## -remarks



The E_INK_OVERLAPPING_INPUT_RECT error is returned if the window input rectangle of an enabled ink collector (set with the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> property) overlaps the window input rectangle of another enabled ink collector.

<div class="alert"><b>Note</b>  Overlap can occur without an error as long as only one of the input rectangles is enabled at any known time.</div>
<div> </div>
By default, the window input rectangle is set to {0,0,0,0}. This default rectangle maps to the size of the entire window.

To reset the window input rectangle to its default behavior (an empty rectangle with coordinates {0,0,0,0}), pass {0,0,0,0} in the call to <b>SetWindowInputRectangle</b>, and not <b>NULL</b>.

You cannot pass in a rectangle where the value of the <a href="https://msdn.microsoft.com/c31fd527-a6aa-4017-bc51-cedca42817f9">Right</a> property is less than the value of the <a href="https://msdn.microsoft.com/88f0d919-43d0-408f-97f8-1410b2833269">Left</a> property; or where the value of the <a href="https://msdn.microsoft.com/9b388cdb-66b1-4386-a1aa-578f0d56c190">Bottom</a> property is less than the value of the <a href="https://msdn.microsoft.com/f97145cf-9de9-427a-9701-36c6f4286910">Top</a> property. For example, a rectangle with parameters of {500, 500, 400, 400} is not valid.

<div class="alert"><b>Caution</b>  If you set the window input rectangle to overlap a splitter control or the borders of the window, unpredictable results may occur when the window is resized.</div>
<div> </div>
<div class="alert"><b>Note</b>  Calling this method within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt+TAB or Alt+ESC key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled Property</a>



<a href="https://msdn.microsoft.com/0f47b4c7-7ba1-44a6-8f62-9e97c318bd2c">GetWindowInputRectangle Method</a>



<a href="tablet.iinkcollector">IInkCollector</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>
 

 

