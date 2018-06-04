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

# IPhotoAcquireSettings::GetSequenceZeroPadding


## -description



The <code>GetSequenceZeroPadding</code> method retrieves a value that indicates whether zeros or spaces will be used to pad sequential file names.




## -parameters




### -param pfZeroPad [out]

Pointer to a flag that, if set to <b>TRUE</b>, indicates that zeros will pad sequential file names.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



A file name padded with zeros might appear as


<pre class="syntax" xml:space="preserve"><code>"IMG0001.JPG"</code></pre>


The same file name without zero padding might appear as 


<pre class="syntax" xml:space="preserve"><code>"IMG   1.JPG"</code></pre>





## -see-also




<a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings Interface</a>



<a href="https://msdn.microsoft.com/5010a61f-a01c-4dd9-850e-581a62b31ab4">SetSequenceZeroPadding</a>
 

 

