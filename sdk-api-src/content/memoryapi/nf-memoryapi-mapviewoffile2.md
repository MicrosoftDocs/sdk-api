---
UID: NF:memoryapi.MapViewOfFile2
title: MapViewOfFile2 function (memoryapi.h)
description: Maps a view of a file or a pagefile-backed section into the address space of the specified process.
helpviewer_keywords: ["MapViewOfFile2","MapViewOfFile2 function","base.mapviewoffile2","winbase/MapViewOfFile2"]
old-location: base\mapviewoffile2.htm
tech.root: base
ms.assetid: D97138F0-2FB3-488A-91AC-A654B22FE9AD
ms.date: 12/05/2018
ms.keywords: MapViewOfFile2, MapViewOfFile2 function, base.mapviewoffile2, winbase/MapViewOfFile2
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
req.lib: kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MapViewOfFile2
 - memoryapi/MapViewOfFile2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - MapViewOfFile2
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
                    will be mapped. The handle must have the <b>PROCESS_VM_OPERATION</b> access mask.

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
<li><b>MEM_RESERVE</b> - Maps a reserved view.</li>
<li><b>MEM_LARGE_PAGES</b> - Maps a large page view. This flag specifies that the view should be mapped using <a href="/windows/win32/memory/large-page-support">large page support</a>. The size of the view must be a multiple of the size of a large page reported by the <a href="/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum">GetLargePageMinimum</a> function, and the file-mapping object must have been created using the <b>SEC_LARGE_PAGES</b> option. If you provide a non-null value for the <i>BaseAddress</i> parameter, then the value must be a multiple of <b>GetLargePageMinimum</b>.</li>
</ul>

### -param PageProtection [in]

The desired page protection.

For file-mapping objects created with the <b>SEC_IMAGE</b> attribute, the 
       <i>PageProtection</i> parameter has no effect, and should be set to any valid value such as 
       <b>PAGE_READONLY</b>.

## -returns

Returns the base address of the mapped view, if successful. Otherwise, returns <b>NULL</b> and extended error status is available
           using <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is implemented as an inline function in the header and can't be found in any export library or DLL. It's the same as calling <a href="/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffilenuma2">MapViewOfFileNuma2</a> with the last parameter set to ``NUMA_NO_PREFERRED_NODE``.

## -see-also

<a href="/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>



<a href="/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffilenuma2">MapViewOfFileNuma2</a>
