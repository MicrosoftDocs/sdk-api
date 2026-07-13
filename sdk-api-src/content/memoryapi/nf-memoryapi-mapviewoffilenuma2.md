---
UID: NF:memoryapi.MapViewOfFileNuma2
title: MapViewOfFileNuma2 function (memoryapi.h)
description: Maps a view of a file or a pagefile-backed section into the address space of the specified process. (MapViewOfFileNuma2)
helpviewer_keywords: ["MapViewOfFileNuma2","MapViewOfFileNuma2 function","base.mapviewoffilenuma2","winbase/MapViewOfFileNuma2"]
old-location: base\mapviewoffilenuma2.htm
tech.root: base
ms.assetid: 848BF3AD-9469-4A16-B1C4-B5D78954D9B5
ms.date: 12/05/2018
ms.keywords: MapViewOfFileNuma2, MapViewOfFileNuma2 function, base.mapviewoffilenuma2, winbase/MapViewOfFileNuma2
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
req.lib: Onecore.lib; Onecoreuap.lib
req.dll: Api-ms-win-core-memory-l1-1-5.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MapViewOfFileNuma2
 - memoryapi/MapViewOfFileNuma2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
api_name:
 - MapViewOfFileNuma2
---

# MapViewOfFileNuma2 function


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

The number of bytes to map. A value of zero
               (0) specifies that the entire section is to be mapped.

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

### -param PreferredNode [in]

The preferred NUMA node for this memory.

## -returns

Returns the base address of the mapped view, if successful. Otherwise, returns <b>NULL</b> and extended error status is available
           using <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffilenuma2">MapViewOfFileNuma</a>
