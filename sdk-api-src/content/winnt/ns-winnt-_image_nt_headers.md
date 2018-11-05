---
UID: NS:winnt._IMAGE_NT_HEADERS
title: "_IMAGE_NT_HEADERS"
author: windows-sdk-content
description: Represents the PE header format.
old-location: base\image_nt_headers_str.htm
tech.root: debug
ms.assetid: 6511341f-252d-4f73-bb90-284bbb69b065
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PIMAGE_NT_HEADERS32, IMAGE_NT_HEADERS, IMAGE_NT_HEADERS structure, IMAGE_NT_HEADERS32, IMAGE_NT_HEADERS64, PIMAGE_NT_HEADERS, PIMAGE_NT_HEADERS structure pointer, _IMAGE_NT_HEADERS, _win32_image_nt_headers_str, base.image_nt_headers_str, winnt/IMAGE_NT_HEADERS, winnt/PIMAGE_NT_HEADERS"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: IMAGE_NT_HEADERS32, *PIMAGE_NT_HEADERS32
req.redist: 
---

# _IMAGE_NT_HEADERS structure


## -description


Represents the PE header format.


## -struct-fields




### -field Signature

A 4-byte signature identifying the file as a PE image. The bytes are "PE\0\0".


### -field FileHeader

An 
<a href="https://msdn.microsoft.com/1f1fe842-0849-46d0-8dba-831cf5aa02ef">IMAGE_FILE_HEADER</a> structure that specifies the file header.


### -field OptionalHeader

An 
<a href="https://msdn.microsoft.com/b6a50ffc-49f8-4824-9b51-7e381eaf8852">IMAGE_OPTIONAL_HEADER</a> structure that specifies the optional file header.


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




<a href="https://msdn.microsoft.com/01a99601-64de-412d-991e-b1708286ca8c">CheckSumMappedFile</a>



<a href="https://msdn.microsoft.com/1f1fe842-0849-46d0-8dba-831cf5aa02ef">IMAGE_FILE_HEADER</a>



<a href="https://msdn.microsoft.com/b6a50ffc-49f8-4824-9b51-7e381eaf8852">IMAGE_OPTIONAL_HEADER</a>



<a href="https://msdn.microsoft.com/b88c7a21-933f-450c-97e8-04cf3c5f9b11">ImageHlp Structures</a>



<a href="https://msdn.microsoft.com/bf796c81-84d1-43e6-a2ff-b0be6f4603e0">ImageNtHeader</a>



<a href="https://msdn.microsoft.com/a11df748-242b-4dd8-bf57-7ac02548b701">ImageRvaToSection</a>



<a href="https://msdn.microsoft.com/7f022054-d98e-44c8-b256-5c34711ce471">ImageRvaToVa</a>



<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a>



<a href="https://msdn.microsoft.com/b29026e2-3063-447c-9449-7105deb3d744">UpdateDebugInfoFile</a>
 

 

