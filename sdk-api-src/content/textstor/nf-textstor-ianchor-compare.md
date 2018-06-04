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

# IAnchor::Compare


## -description


The <b>IAnchor::Compare</b> method compares the relative position of two anchors within a text stream.


## -parameters




### -param paWith [in]

An anchor object to compare to the primary anchor. Used to determine the relative position of the two anchors.


### -param plResult [out]

Result of the comparison of the positions of the two anchors.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="-1"></a><dl>
<dt><b>-1</b></dt>
</dl>
</td>
<td width="60%">
The primary anchor is positioned earlier in the text stream than <i>paWith.</i>

</td>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The primary anchor is positioned at the same location as <i>paWith.</i>

</td>
</tr>
<tr>
<td width="40%"><a id="_1"></a><dl>
<dt><b>+1</b></dt>
</dl>
</td>
<td width="60%">
The primary anchor is positioned later in the text stream than <i>paWith.</i>

</td>
</tr>
</table>
 


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
<i>paWith</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>plResult</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



The value 0 is returned for <i>*plResult</i> only when the two anchors are in a single region. Anchor positions include the spaces between regions. If you only need to determine if the two anchors are positioned at the same location, <a href="https://msdn.microsoft.com/a2dedce7-f64d-406a-bebc-9a4b51a1ae38">IAnchor::IsEqual</a> is more efficient.




## -see-also




<a href="ranges.htm">Anchors</a>



<a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a>



<a href="https://msdn.microsoft.com/a2dedce7-f64d-406a-bebc-9a4b51a1ae38">IAnchor::IsEqual
      </a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn915768">Regions</a>
 

 

