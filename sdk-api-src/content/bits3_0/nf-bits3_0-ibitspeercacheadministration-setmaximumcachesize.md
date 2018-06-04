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

# IBitsPeerCacheAdministration::SetMaximumCacheSize


## -description


Specifies the maximum size of the cache.


## -parameters




### -param Bytes [in]

Maximum size of the cache, as a percentage of available hard disk drive space.


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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The configuration preference has been saved successfully, but the preference will not be used because a configured Group Policy setting overrides the preference.

</td>
</tr>
</table>
 




## -remarks



This value is used only if the MaxCacheSize group policy is not set.

If the maximum cache size is reached, BITS removes the least recently accessed files until the necessary disk space is freed. If you specify a value that is less than the current cache size, BITS removes files from the cache until the requested size is met. BITS removes the files based on <a href="https://msdn.microsoft.com/815d9e48-f1f0-4c40-a277-d78db9d6ace1">age</a>. Files that are larger than the cache size are not cached.

By default, the maximum cache size is 1% of the disk size.    BITS does not use the limit to reserve disk space for the cache. BITS will use up to the specified limit for the cache, if the disk space is available. The maximum value you can specify is 80% of the disk size.

If the request is to reduce the size of the cache and BITS is currently downloading a file from the cache, BITS will not remove the file until the download is complete.




## -see-also




<a href="https://msdn.microsoft.com/5fa30b4e-f13c-4341-af65-a2e3d2703b96">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/6ea0e6f7-c674-4088-9085-5f6246681009">IBitsPeerCacheAdministration::GetMaximumCacheSize</a>



<a href="https://msdn.microsoft.com/815d9e48-f1f0-4c40-a277-d78db9d6ace1">IBitsPeerCacheAdministration::SetMaximumContentAge</a>
 

 

