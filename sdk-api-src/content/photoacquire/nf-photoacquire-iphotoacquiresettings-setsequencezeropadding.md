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

# IPhotoAcquireSettings::SetSequenceZeroPadding


## -description



The <code>SetSequenceZeroPadding</code> method sets a value indicating whether zeros or spaces are used to pad sequential file names.




## -parameters




### -param fZeroPad [in]

Flag that, if set to <b>TRUE</b>, indicates that zeros pad sequential file names.


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




<a href="https://msdn.microsoft.com/72dc052a-bf8e-4876-8ab6-d0f6857941d5">GetSequenceZeroPadding</a>



<a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings Interface</a>



<a href="https://msdn.microsoft.com/2c90c109-1522-4722-a691-6f0f3caa50ec">SetSequencePaddingWidth</a>
 

 

