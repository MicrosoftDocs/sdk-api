---
UID: NF:msinkaut.IInkStrokeDisp.GetPoints
title: IInkStrokeDisp::GetPoints
author: windows-sdk-content
description: Retrieves the points that make up a stroke.
old-location: tablet\iinkstrokedisp_getpoints.htm
tech.root: tablet
ms.assetid: 76378521-15d1-48a0-ae9f-8362faf60c9f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 76378521-15d1-48a0-ae9f-8362faf60c9f, GetPoints, GetPoints method [Tablet PC], GetPoints method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],GetPoints method, IInkStrokeDisp.GetPoints, IInkStrokeDisp::GetPoints, msinkaut/IInkStrokeDisp::GetPoints, tablet.iinkstrokedisp_getpoints
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
 - IInkStrokeDisp.GetPoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkStrokeDisp::GetPoints


## -description



Retrieves the points that make up a stroke.




## -parameters




### -param Index [in, optional]

Optional. The starting index within the array of points that make up the stroke. The default value ISC_FirstElement, defined in the <a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ItemSelectionConstants</a> enumeration type, specifies the first point.


### -param Count [in, optional]

Optional. The number of points to return. The default value ISC_AllElements, defined in the <a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ItemSelectionConstants</a> enumeration type, specifies all of the points that make up the stroke data.


### -param Points [out, retval]

Whent this method returns, contains the array of points from the stroke.

For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory for the points.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid index (out of range).

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ItemSelectionConstants Enumeration</a>
 

 

