---
UID: NN:msinkaut15.IInkDivider
title: IInkDivider
author: windows-sdk-content
description: "."
old-location: tablet\iinkdivider.htm
tech.root: tablet
ms.assetid: 6DF54C8E-1E0D-4F9D-A6E4-AFE0E8894BE9
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IInkDivider, IInkDivider interface [Tablet PC], IInkDivider interface [Tablet PC],described, msinkaut15/IInkDivider, tablet.iinkdivider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msinkaut15.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut15.h
api_name:
 - IInkDivider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDivider interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkDivider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkDivider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be42ac65-2bde-4439-a82b-3453c0737717">Divide</a>
</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/d1a71976-2825-48d2-812c-fd2336cd4c1d">IInkDivisionResult</a> object that contains the results of the layout analysis of strokes in the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/69e65ad6-bcee-46a7-a139-80b4324b9c72">LineHeight</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the expected handwriting height, in HIMETRIC units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ad3c4317-a777-4009-bc66-865a2fcb77c3">RecognizerContext</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object that the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object uses for layout analysis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/611ccce9-7acb-4138-9655-938efcaa4c75">Strokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection on which the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object performs layout analysis.

</td>
</tr>
</table> 

