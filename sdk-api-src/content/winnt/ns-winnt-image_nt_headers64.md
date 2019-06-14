---
UID: NS:winnt._IMAGE_NT_HEADERS64
title: IMAGE_NT_HEADERS64 (winnt.h)
author: windows-sdk-content
description: Represents the PE header format.
old-location: base\image_nt_headers_str.htm
tech.root: Debug
ms.assetid: 6511341f-252d-4f73-bb90-284bbb69b065
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PIMAGE_NT_HEADERS64, IMAGE_NT_HEADERS, IMAGE_NT_HEADERS structure, IMAGE_NT_HEADERS32, IMAGE_NT_HEADERS64, PIMAGE_NT_HEADERS, PIMAGE_NT_HEADERS structure pointer, _IMAGE_NT_HEADERS, _win32_image_nt_headers_str, base.image_nt_headers_str, winnt/IMAGE_NT_HEADERS, winnt/PIMAGE_NT_HEADERS"
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - IMAGE_NT_HEADERS
product: Windows
targetos: Windows
req.typenames: IMAGE_NT_HEADERS64, *PIMAGE_NT_HEADERS64
req.redist: 
ms.custom: 19H1
---

# IMAGE_NT_HEADERS64 structure


## -description


Represents the PE header format.


## -struct-fields




### -field Signature

A 4-byte signature identifying the file as a PE image. The bytes are "PE\0\0".


### -field FileHeader

An 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_image_file_header">IMAGE_FILE_HEADER</a> structure that specifies the file header.


### -field OptionalHeader

An 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_image_optional_header">IMAGE_OPTIONAL_HEADER</a> structure that specifies the optional file header.


## -remarks



The actual structure in WinNT.h is named <b>IMAGE_NT_HEADERS32</b> and <b>IMAGE_NT_HEADERS</b> is defined as <b>IMAGE_NT_HEADERS32</b>. However, if _WIN64 is defined,  then <b>IMAGE_NT_HEADERS</b> is defined as <b>IMAGE_NT_HEADERS64</b>.


```cpp
typedef struct _IMAGE_NT_HEADERS64 {
    DWORD Signature;
    IMAGE_FILE_HEADER FileHeader;
    IMAGE_OPTIONAL_HEADER64 OptionalHeader;
} IMAGE_NT_HEADERS64, *PIMAGE_NT_HEADERS64;
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imagehlp/nf-imagehlp-checksummappedfile">CheckSumMappedFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_image_file_header">IMAGE_FILE_HEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_image_optional_header">IMAGE_OPTIONAL_HEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/Debug/imagehlp-structures">ImageHlp Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-imagentheader">ImageNtHeader</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-imagervatosection">ImageRvaToSection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-imagervatova">ImageRvaToVa</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/ns-dbghelp-_loaded_image">LOADED_IMAGE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imagehlp/nf-imagehlp-updatedebuginfofile">UpdateDebugInfoFile</a>
 

 

