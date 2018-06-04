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

# IInkDivisionResult::ResultByType


## -description



Gets the requested structural units of the analysis results for an <a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">IInkDivisionUnits</a> collection.




## -parameters




### -param divisionType [in]

The <a href="https://msdn.microsoft.com/00e1188e-58c0-4681-ad04-e53079d478fd">InkDivisionType</a> enumeration value that indicates the structural units to return.


### -param InkDivisionUnits [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">IInkDivisionUnits</a> collection that contains the requested structural units of the analysis results.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains an invalid value.

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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -remarks



This method returns a new <a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">IInkDivisionUnits</a> collection each time the method is called.

If no structural units of the requested type exist in the <a href="https://msdn.microsoft.com/d1a71976-2825-48d2-812c-fd2336cd4c1d">IInkDivisionResult</a> object, then this method returns an empty <a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">IInkDivisionUnits</a> collection.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/d1a71976-2825-48d2-812c-fd2336cd4c1d">IInkDivisionResult Interface</a>



<a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">IInkDivisionUnits Interface</a>



<a href="https://msdn.microsoft.com/00e1188e-58c0-4681-ad04-e53079d478fd">InkDivisionType Enumeration</a>
 

 

