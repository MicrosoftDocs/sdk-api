---
UID: NF:msinkaut15.IInkDivider.Divide
title: IInkDivider::Divide
author: windows-sdk-content
description: Returns a IInkDivisionResult object that contains the results of the layout analysis of strokes in the InkDivider object.
old-location: tablet\inkdivider_divide.htm
tech.root: tablet
ms.assetid: be42ac65-2bde-4439-a82b-3453c0737717
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: Divide, Divide method [Tablet PC], Divide method [Tablet PC],IInkDivider interface, IInkDivider, IInkDivider interface [Tablet PC],Divide method, IInkDivider.Divide, IInkDivider::Divide, be42ac65-2bde-4439-a82b-3453c0737717, msinkaut15/IInkDivider::Divide, tablet.inkdivider_divide
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut15.h
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
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inkdiv.dll
 - Inkdiv.dll.dll
api_name:
 - IInkDivider.Divide
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDivider::Divide


## -description



Returns a <a href="https://msdn.microsoft.com/d1a71976-2825-48d2-812c-fd2336cd4c1d">IInkDivisionResult</a> object that contains the results of the layout analysis of strokes in the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object.




## -parameters




### -param InkDivisionResult [out, retval]

When this method returns, contains a pointer to an <a href="https://msdn.microsoft.com/d1a71976-2825-48d2-812c-fd2336cd4c1d">IInkDivisionResult</a> object that contains structural information about the strokes in the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to complete the operation.

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
</table>
 




## -remarks



This method returns a new <a href="https://msdn.microsoft.com/d1a71976-2825-48d2-812c-fd2336cd4c1d">IInkDivisionResult</a> object each time this method is called.




## -see-also




<a href="https://msdn.microsoft.com/6DF54C8E-1E0D-4F9D-A6E4-AFE0E8894BE9">IInkDivider</a>



<a href="https://msdn.microsoft.com/d1a71976-2825-48d2-812c-fd2336cd4c1d">IInkDivisionResult Interface</a>



<a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider Class</a>
 

 

