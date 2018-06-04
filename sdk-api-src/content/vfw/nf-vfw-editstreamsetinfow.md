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

# EditStreamSetInfoW function


## -description



The <b>EditStreamSetInfo</b> function changes characteristics of an editable stream.




## -parameters




### -param pavi

Handle to an open stream.


### -param lpInfo

Pointer to an <a href="https://msdn.microsoft.com/dca6d9ca-a825-4bd0-a19d-0655d775fdfb">AVISTREAMINFO</a> structure containing new information.


### -param cbInfo

Size, in bytes, of the structure pointed to by <i>lpInfo</i>.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



You must supply information for the entire <a href="https://msdn.microsoft.com/dca6d9ca-a825-4bd0-a19d-0655d775fdfb">AVISTREAMINFO</a> structure, including the members you will not use. You can use the <a href="https://msdn.microsoft.com/7a1ba29b-e8ba-435d-a551-c9184631971c">AVIStreamInfo</a> function to initialize the structure and then update selected members with your data.

This function does not change the following members:

<ul>
<li><b>dwCaps</b></li>
<li><b>dwEditCount</b></li>
<li><b>dwFlags</b></li>
<li><b>dwInitialFrames</b></li>
<li><b>dwLength</b></li>
<li><b>dwSampleSize</b></li>
<li><b>dwSuggestedBufferSize</b></li>
<li><b>fccHandler</b></li>
<li><b>fccType</b></li>
</ul>
The function changes the following members:

<ul>
<li><b>dwRate</b></li>
<li><b>dwQuality</b></li>
<li><b>dwScale</b></li>
<li><b>dwStart</b></li>
<li><b>rcFrame</b></li>
<li><b>szName</b></li>
<li><b>wLanguage</b></li>
<li><b>wPriority</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

