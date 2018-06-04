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

# _MINIDUMP_USER_STREAM_INFORMATION structure


## -description


Contains a list of user data streams used by the 
<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a> function.


## -struct-fields




### -field UserStreamCount

The number of user streams.


### -field UserStreamArray

An array of 
<a href="https://msdn.microsoft.com/43eae98c-fba3-43a4-97e6-8b81874e856e">MINIDUMP_USER_STREAM</a> structures.


## -remarks



In this context, a data stream refers to a block of data within a minidump file.




## -see-also




<a href="https://msdn.microsoft.com/43eae98c-fba3-43a4-97e6-8b81874e856e">MINIDUMP_USER_STREAM</a>



<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a>
 

 

