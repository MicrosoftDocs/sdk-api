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

# IFont::ReleaseHfont


## -description


Notifies the font object that the caller that previously locked this font in the cache with 
   <a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">IFont::AddRefHfont</a> no longer requires the lock.


## -parameters




### -param hFont [in]

A font handle previously realized through 
      <a href="https://msdn.microsoft.com/19bfd78a-0e81-45c3-a3b8-bc893669e9f5">IFont::get_hFont</a>. This value was passed to a previous 
      call to <a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">IFont::AddRefHfont</a> to lock the font, and the 
      caller would now like to unlock the font in the cache.


## -returns



The method supports the standard return values <b>E_UNEXPECTED</b> and 
      <b>E_INVALIDARG</b>, as well as the following values.

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
The font was unlocked successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The font was not locked in the cache. This return value is a benign notification to the caller that it 
        may have a font reference counting problem.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">IFont::AddRefHfont</a>
 

 

