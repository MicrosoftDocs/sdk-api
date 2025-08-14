---
UID: NF:winddi.EngMapFile
title: EngMapFile function (winddi.h)
description: The EngMapFile function creates or opens a file and maps it into system space.
helpviewer_keywords: ["EngMapFile","EngMapFile function [Display Devices]","display.engmapfile","gdifncs_efc9de46-c5dc-446b-9686-8cf868bfa1e9.xml","winddi/EngMapFile"]
old-location: display\engmapfile.htm
tech.root: display
ms.assetid: 6887f7e1-f94f-421c-be7a-14a41d621ce1
ms.date: 12/05/2018
ms.keywords: EngMapFile, EngMapFile function [Display Devices], display.engmapfile, gdifncs_efc9de46-c5dc-446b-9686-8cf868bfa1e9.xml, winddi/EngMapFile
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngMapFile
 - winddi/EngMapFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngMapFile
---

# EngMapFile function


## -description

The <b>EngMapFile</b> function creates or opens a file and maps it into <a href="/windows-hardware/drivers/">system space</a>.

## -parameters

### -param pwsz [in]

Pointer to a null-terminated string that contains the fully qualified name of the file to be mapped. An example of a fully qualified file name string is <i>L"\\??\\c:\\test.dat".</i>

### -param cjSize [in]

Specifies the number of bytes of the file to map.

### -param piFile [out]

Pointer to a memory location that receives an identifier for the mapped file, provided that the mapping succeeded. If the mapping did not succeed, the memory location receives the value zero. When the mapped file needs to be released, this value should be passed to <a href="/windows/desktop/api/winddi/nf-winddi-engunmapfile">EngUnmapFile</a>.

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

<a href="/windows/desktop/api/winddi/nf-winddi-engdeletefile">EngDeleteFile</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engunmapfile">EngUnmapFile</a>