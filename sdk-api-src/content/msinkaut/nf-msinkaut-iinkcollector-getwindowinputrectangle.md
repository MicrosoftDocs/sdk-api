---
UID: NF:msinkaut.IInkCollector.GetWindowInputRectangle
title: IInkCollector::GetWindowInputRectangle
author: windows-sdk-content
description: Gets the window rectangle, in pixels, within which ink is drawn.
old-location: tablet\inkcollector_getwindowinputrectangle.htm
tech.root: tablet
ms.assetid: 0f47b4c7-7ba1-44a6-8f62-9e97c318bd2c
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: 0f47b4c7-7ba1-44a6-8f62-9e97c318bd2c, GetWindowInputRectangle, GetWindowInputRectangle method [Tablet PC], GetWindowInputRectangle method [Tablet PC],IInkCollector interface, IInkCollector interface [Tablet PC],GetWindowInputRectangle method, IInkCollector.GetWindowInputRectangle, IInkCollector::GetWindowInputRectangle, msinkaut/IInkCollector::GetWindowInputRectangle, tablet.inkcollector_getwindowinputrectangle
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkCollector.GetWindowInputRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkCollector::GetWindowInputRectangle


## -description



Gets the window rectangle, in pixels, within which ink is drawn.




## -parameters




### -param WindowInputRectangle [out]

 The rectangle, of type <a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle</a>, on which ink is drawn.


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
A parameter contains an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The InkRectangle object is not registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurs inside the method.

</td>
</tr>
</table>
 




## -remarks



You must first allocate the rectangle before passing it on to this method.

By default, the window input rectangle is set to {0,0,0,0}. This default rectangle maps to the size of the entire window.

If you call <b>GetWindowInputRectangle</b> before you call the <a href="https://msdn.microsoft.com/b46139db-0473-4cd3-8f1b-d303f3430470">SetWindowInputRectangle</a> method, this method gets a rectangle with the default coordinates.




## -see-also




<a href="https://msdn.microsoft.com/4E539E4F-2E7F-44ED-A8D0-650BCAFDFAFB">IInkCollector</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/b46139db-0473-4cd3-8f1b-d303f3430470">SetWindowInputRectangle Method</a>
 

 

