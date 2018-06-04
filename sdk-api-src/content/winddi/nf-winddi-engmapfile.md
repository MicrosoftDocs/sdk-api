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

# EngMapFile function


## -description


The <b>EngMapFile</b> function creates or opens a file and maps it into <a href="https://msdn.microsoft.com/5f6fec1a-1134-4765-81be-9b50939e5e66">system space</a>.


## -parameters




### -param pwsz [in]

Pointer to a null-terminated string that contains the fully qualified name of the file to be mapped. An example of a fully qualified file name string is <i>L"\\??\\c:\\test.dat".</i>


### -param cjSize [in]

Specifies the number of bytes of the file to map.


### -param piFile [out]

Pointer to a memory location that receives an identifier for the mapped file, provided that the mapping succeeded. If the mapping did not succeed, the memory location receives the value zero. When the mapped file needs to be released, this value should be passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff565437">EngUnmapFile</a>.


## -returns



<b>EngMapFile</b> returns a pointer to the mapped view of the file if it succeeds. Otherwise, it returns <b>NULL</b>.




## -remarks



If the file already exists, <b>EngMapFile</b> opens and maps it for read/write. If the file does not exist, <b>EngMapFile</b> creates and maps it for read/write.

The value of <i>cjSize</i> affects the mapping of the file as follows:

<ul>
<li>
When <i>cjSize</i> is zero, GDI maps the file in its entirety.

</li>
<li>
When <i>cjSize</i> is greater than the size of the file, GDI expands the file to <i>cjSize</i> bytes in size before mapping it in system memory. No assumptions should be made about the contents of memory that extend beyond the file's original size.

</li>
<li>
When <i>cjSize</i> is less than the size of the file, GDI truncates the file to <i>cjSize</i> bytes in size before mapping it into system memory.

</li>
</ul>
A driver can read and write to the file through the returned pointer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564803">EngDeleteFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565437">EngUnmapFile</a>
 

 

