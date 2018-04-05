---
UID: NF:msinkaut15.IInkDivisionResult.ResultByType
title: IInkDivisionResult::ResultByType method
author: windows-driver-content
description: Gets the requested structural units of the analysis results for an IInkDivisionUnits collection.
old-location: tablet\iinkdivisionresult_resultbytype.htm
old-project: tablet
ms.assetid: d0bad0e8-e48c-443b-b52e-e95de3158710
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IInkDivisionResult, IInkDivisionResult interface [Tablet PC], ResultByType method, IInkDivisionResult::ResultByType, ResultByType method [Tablet PC], ResultByType method [Tablet PC], IInkDivisionResult interface, ResultByType,IInkDivisionResult.ResultByType, d0bad0e8-e48c-443b-b52e-e95de3158710, msinkaut15/IInkDivisionResult::ResultByType, tablet.iinkdivisionresult_resultbytype
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
req.typenames: InkRecoGuide
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Inkdiv.dll
-	Inkdiv.dll.dll
api_name:
-	IInkDivisionResult.ResultByType
product: Windows
targetos: Windows
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkDivisionResult::ResultByType method


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
 

 

