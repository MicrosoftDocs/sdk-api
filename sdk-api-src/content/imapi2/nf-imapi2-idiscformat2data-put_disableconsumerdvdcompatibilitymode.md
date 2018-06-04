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

# IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode


## -description


Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD.


## -parameters




### -param value [in]

Set to VARIANT_TRUE to skip the tasks that allow the disc to play on more consumer devices. Removing compatibility reduces the  recording session time and the need for less free space on disc.

Set to VARIANT_FALSE to increase the chance that a device can play the DVD. The default is VARIANT_FALSE.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is currently a write operation in progress.

Value: 0xC0AA0400

</td>
</tr>
</table>
 




## -remarks



This property has no affect on CD media and DVD dash media.

For DVD+R and DVD+DL media, this property will also affect the media closing operation. 

<table>
<tr>
<th>Value of DisableConsumerDvdCompatibilityMode </th>
<th>Value of ForceMediaToBeClosed </th>
<th>Closure operation</th>
</tr>
<tr>
<td>False</td>
<td>True</td>
<td>Closes the disc in compatible mode</td>
</tr>
<tr>
<td>Fale</td>
<td>False</td>
<td>Closes the disc in compatible mode</td>
</tr>
<tr>
<td>True</td>
<td>True</td>
<td>Closes the disc normally</td>
</tr>
<tr>
<td>True</td>
<td>False</td>
<td>Closes the session for DVD+RCloses disc normally for DVD+R DL 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/dc88f657-0ec1-488d-8110-055de06c2d58">IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode</a>
 

 

