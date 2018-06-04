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

# ITextSelection::GetType


## -description


Gets the type of text selection.


## -parameters




### -param pType

Type: <b>long*</b>

The selection type. The method returns <i>pType</i> with one of the values in the following table.


<table class="clsStd">
<tr>
<th>Selection type</th>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomNoSelection</b></td>
<td>0</td>
<td>No selection and no insertion point.</td>
</tr>
<tr>
<td><b>tomSelectionIP</b></td>
<td>1</td>
<td>Insertion point.</td>
</tr>
<tr>
<td><b>tomSelectionNormal</b></td>
<td>2</td>
<td>Single nondegenerate range.</td>
</tr>
<tr>
<td><b>tomSelectionFrame</b></td>
<td>3</td>
<td>Frame.</td>
</tr>
<tr>
<td><b>tomSelectionColumn</b></td>
<td>4</td>
<td>Table column.</td>
</tr>
<tr>
<td><b>tomSelectionRow</b></td>
<td>5</td>
<td>Table rows.</td>
</tr>
<tr>
<td><b>tomSelectionBlock</b></td>
<td>6</td>
<td>Block selection.</td>
</tr>
<tr>
<td><b>tomSelectionInlineShape</b></td>
<td>7</td>
<td>Picture.</td>
</tr>
<tr>
<td><b>tomSelectionShape</b></td>
<td>8</td>
<td>Shape.</td>
</tr>
</table>
 


## -returns



Type: <b>StdMETHODIMP</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pType</i> is null, the method fails and it returns E_INVALIDARG.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e6afce18-4f02-4f1c-a2ee-735465d2e168">ITextSelection</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

