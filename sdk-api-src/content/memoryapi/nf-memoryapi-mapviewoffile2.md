---
UID: NF:memoryapi.MapViewOfFile2
title: MapViewOfFile2 function
author: windows-sdk-content
description: Maps a view of a file or a pagefile-backed section into the address space of the specified process.
old-location: base\mapviewoffile2.htm
tech.root: memory
ms.assetid: D97138F0-2FB3-488A-91AC-A654B22FE9AD
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: MapViewOfFile2, MapViewOfFile2 function, base.mapviewoffile2, winbase/MapViewOfFile2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - MapViewOfFile2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MapViewOfFile2 function


## -description


Maps a view of a file or a pagefile-backed section into the address
    space of the specified process.


## -parameters




### -param FileMappingHandle [in]

A <b>HANDLE</b> to a section that is to be mapped
                        into the address space of the specified process.


### -param ProcessHandle [in]

A <b>HANDLE</b> to a process into which the section
                    will be mapped.


### -param Offset [in]

The offset from the beginning of the section.
             This must be 64k aligned.


### -param BaseAddress [in, optional]

The desired base address of the view.
                  The address is rounded down to the nearest 64k boundary.
                  If this parameter is <b>NULL</b>, the system picks the base
                  address.


### -param ViewSize [in]

The number of bytes to map. A value of zero (0)
               specifies that the entire section is to be mapped.


### -param AllocationType [in]

The type of allocation. This parameter can be zero (0) or one of the following constant values:

<ul>
<li><b>MEM_RESERVE</b> - Maps a reserved view</li>
<li><b>MEM_LARGE_PAGES</b> - Maps a large page view</li>
</ul>

### -param PageProtection [in]

The desired page protection.

For file-mapping objects created with the <b>SEC_IMAGE</b> attribute, the 
       <i>PageProtection</i> parameter has no effect, and should be set to any valid value such as 
       <b>PAGE_READONLY</b>.


## -returns



Returns the base address of the mapped view, if successful. Otherwise, returns <b>NULL</b> and extended error status is available
           using <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>



<a href="https://msdn.microsoft.com/848BF3AD-9469-4A16-B1C4-B5D78954D9B5">MapViewOfFileNuma2</a>
 

 

