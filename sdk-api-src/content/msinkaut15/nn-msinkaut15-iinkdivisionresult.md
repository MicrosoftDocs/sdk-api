---
UID: NN:msinkaut15.IInkDivisionResult
title: IInkDivisionResult
author: windows-driver-content
description: Represents the layout analysis of the collection of strokes contained by the InkDivider object.
old-location: tablet\iinkdivisionresult.htm
old-project: tablet
ms.assetid: d1a71976-2825-48d2-812c-fd2336cd4c1d
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IInkDivisionResult, IInkDivisionResult interface [Tablet PC], IInkDivisionResult interface [Tablet PC], described, d1a71976-2825-48d2-812c-fd2336cd4c1d, msinkaut15/IInkDivisionResult, tablet.iinkdivisionresult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IInkDivisionResult
product: Windows
targetos: Windows
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkDivisionResult interface


## -description



Represents the layout analysis of the collection of strokes contained by the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivisionResult</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkDivisionResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkDivisionResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0bad0e8-e48c-443b-b52e-e95de3158710">ResultByType</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">IInkDivisionUnits</a> collection that represents the requested structural units within the analysis result.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivisionResult</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b65f1b71-b0a4-4de2-9321-f660bcd2d3ce">Strokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection that was used to create the analysis results.

</td>
</tr>
</table> 


## -remarks



The <b>IInkDivisionResult</b> object is the result of calling the <a href="https://msdn.microsoft.com/be42ac65-2bde-4439-a82b-3453c0737717">Divide</a> method of the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object. Each <b>IInkDivisionResult</b> represents a snapshot of the layout analysis of the collection of strokes contained by the <b>InkDivider</b>.

The analysis results can be divided into a collection of structural units by calling the <a href="https://msdn.microsoft.com/d0bad0e8-e48c-443b-b52e-e95de3158710">ResultByType</a> method.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">IInkDivisionUnits Interface</a>



<a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>



<a href="https://msdn.microsoft.com/d0bad0e8-e48c-443b-b52e-e95de3158710">ResultByType Method</a>
 

 

