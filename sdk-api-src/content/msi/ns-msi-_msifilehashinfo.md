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

# _MSIFILEHASHINFO structure


## -description


The 
<b>MSIFILEHASHINFO</b> structure contains the file hash information returned by 
<a href="https://msdn.microsoft.com/afd9f0b4-432f-4d23-b59d-7406ac2f68bb">MsiGetFileHash</a> and used in the 
<a href="https://msdn.microsoft.com/972a2784-418d-4cb3-b13c-df89b079e94c">MsiFileHash table</a>.


## -struct-fields




### -field dwFileHashInfoSize

Specifies the size, in bytes, of this data structure. Set this member to <code>sizeof(MSIFILEHASHINFO)</code> before calling the 
<a href="https://msdn.microsoft.com/afd9f0b4-432f-4d23-b59d-7406ac2f68bb">MsiGetFileHash</a> function.


### -field dwData

The entire 128-bit file hash is contained in four 32-bit fields. The first field corresponds to the HashPart1 column of the MsiHashFile table, the second field corresponds to the HashPart2 column, the third field corresponds to the HashPart3 column, and the fourth field corresponds to the HashPart4 column.


## -remarks



The file hash entered into the fields of the MsiFileHash table must be obtained by calling 
<a href="https://msdn.microsoft.com/afd9f0b4-432f-4d23-b59d-7406ac2f68bb">MsiGetFileHash</a> or the 
<a href="https://msdn.microsoft.com/065ffde1-4d7c-4e71-9315-7926d4cd38ed">FileHash method</a>. Do not use other methods to generate a file hash.




## -see-also




<a href="https://msdn.microsoft.com/a09e091c-ee82-4951-b129-d1d4c8948883">Default File Versioning</a>



<a href="https://msdn.microsoft.com/972a2784-418d-4cb3-b13c-df89b079e94c">MsiFileHash table</a>



<a href="https://msdn.microsoft.com/afd9f0b4-432f-4d23-b59d-7406ac2f68bb">MsiGetFileHash</a>
 

 

