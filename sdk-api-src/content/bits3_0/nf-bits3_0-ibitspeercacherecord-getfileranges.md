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

# IBitsPeerCacheRecord::GetFileRanges


## -description


Gets the ranges of the file that are in the cache.


## -parameters




### -param pRangeCount [out]

Number of elements in <i>ppRanges</i>.


### -param ppRanges [out]

Array of  <a href="https://msdn.microsoft.com/4ed20321-fb89-410b-906e-9f2c4366645a">BG_FILE_RANGE</a> structures that specify the ranges of the file that are in the cache. When done, call the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>ppRanges</i>.


## -returns



The method returns the following return values.

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
Success

</td>
</tr>
</table>
 




## -remarks



The method always returns at least one range (for the complete file). Multiple ranges can be returned if the application called <a href="https://msdn.microsoft.com/b3601f23-1a69-47db-8943-7515652cf015">IBackgroundCopyJob3::AddFileWithRanges</a> to download one or more ranges of a file.




## -see-also




<a href="https://msdn.microsoft.com/4ed20321-fb89-410b-906e-9f2c4366645a">BG_FILE_RANGE</a>



<a href="https://msdn.microsoft.com/61db33de-a38c-4c52-9f1b-66d46f25c297">IBitsPeerCacheRecord</a>
 

 

