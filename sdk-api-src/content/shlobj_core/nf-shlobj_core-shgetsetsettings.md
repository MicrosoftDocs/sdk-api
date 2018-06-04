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

# SHGetSetSettings function


## -description


<p class="CCE_Message">[<b>SHGetSetSettings</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sets or retrieves Shell state settings.


## -parameters




### -param lpss [in, out]

Type: <b>LPSHELLSTATE</b>

A pointer to a <a href="https://msdn.microsoft.com/a5ba0e9f-d164-4fe6-97ab-34d61289ce1c">SHELLSTATE</a> structure that provides or receives the Shell state settings.


### -param dwMask [in]

Type: <b>DWORD</b>

One or more of the <a href="https://msdn.microsoft.com/2a883110-fdc3-4451-9e47-e58894600e3b">SSF</a> flags that indicate which settings should be set or retrieved.


### -param bSet [in]

Type: <b>BOOL</b>

<b>TRUE</b> to indicate that the contents of <i>lpss</i> should be used to set the Shell settings, <b>FALSE</b> to indicate that the Shell settings should be retrieved to <i>lpss</i>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/728a4004-f35d-4592-baf1-456a613a3344">SHGetSettings</a>
 

 

