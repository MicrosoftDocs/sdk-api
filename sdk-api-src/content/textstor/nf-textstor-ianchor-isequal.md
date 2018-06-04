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

# IAnchor::IsEqual


## -description


The <b>IAnchor::IsEqual</b> method evaluates two anchors within a text stream and returns a Boolean value that specifies the equality or inequality of the anchor positions.


## -parameters




### -param paWith [in]

Specifies an anchor to compare to the primary anchor. Used to determine the equality of the two anchor positions.


### -param pfEqual [out]

A Boolean value that specifies whether the two anchors are positioned at the same location. If set to <b>TRUE</b>, the two anchors occupy the same location. If set to <b>FALSE</b>, the two anchors do not occupy the same location.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pfEqual</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



Anchors are always positioned between characters or regions. When two anchors are between the same characters, being at the same offset within the text stream, and within the same region, <b>IAnchor::IsEqual</b> returns <b>TRUE</b>. Otherwise it returns <b>FALSE</b>.


<a href="https://msdn.microsoft.com/227ed0c0-0bdd-49af-b5dc-fdb69913b9c1">IAnchor::Compare
        </a> incorporates the same functionality as <b>IAnchor::IsEqual</b>. However, because <b>IAnchor::IsEqual</b> is more specific, it can have a more efficient implementation on the server.




## -see-also




<a href="ranges.htm">Anchors</a>



<a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a>



<a href="https://msdn.microsoft.com/227ed0c0-0bdd-49af-b5dc-fdb69913b9c1">IAnchor::Compare
      </a>
 

 

