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

# IFont::AddRefHfont


## -description


Notifies the font object that the previously realized font identified with <i>hFont</i> should remain valid until <a href="https://msdn.microsoft.com/2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68">ReleaseHfont</a> is called or the font object itself is released completely.


## -parameters




### -param hFont [in]

Font handle previously realized through <a href="https://msdn.microsoft.com/19bfd78a-0e81-45c3-a3b8-bc893669e9f5">get_hFont</a> to be locked in the font object's cache.


## -returns



The method supports the standard return values <b>E_UNEXPECTED</b> and <b>E_INVALIDARG</b>, as well as the following values.

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
The font was successfully locked in the cache.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68">ReleaseHfont</a>



<a href="https://msdn.microsoft.com/19bfd78a-0e81-45c3-a3b8-bc893669e9f5">get_hFont</a>
 

 

