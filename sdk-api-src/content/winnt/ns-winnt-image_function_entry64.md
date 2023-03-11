---
UID: NS:winnt._IMAGE_FUNCTION_ENTRY64
title: IMAGE_FUNCTION_ENTRY64 (winnt.h)
description: Represents an entry in the function table.I
helpviewer_keywords: ["*PIMAGE_FUNCTION_ENTRY64","IMAGE_FUNCTION_ENTRY","IMAGE_FUNCTION_ENTRY structure","IMAGE_FUNCTION_ENTRY64","PIMAGE_FUNCTION_ENTRY","PIMAGE_FUNCTION_ENTRY structure pointer","_IMAGE_FUNCTION_ENTRY","_win32_image_function_entry_str","base.image_function_entry_str","winnt/IMAGE_FUNCTION_ENTRY","winnt/PIMAGE_FUNCTION_ENTRY"]
old-location: base\image_function_entry_str.htm
tech.root: Debug
ms.assetid: ced956ec-7a12-4548-8e38-a1c1057c05e8
ms.date: 12/05/2018
ms.keywords: '*PIMAGE_FUNCTION_ENTRY64, IMAGE_FUNCTION_ENTRY, IMAGE_FUNCTION_ENTRY structure, IMAGE_FUNCTION_ENTRY64, PIMAGE_FUNCTION_ENTRY, PIMAGE_FUNCTION_ENTRY structure pointer, _IMAGE_FUNCTION_ENTRY, _win32_image_function_entry_str, base.image_function_entry_str, winnt/IMAGE_FUNCTION_ENTRY, winnt/PIMAGE_FUNCTION_ENTRY'
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
targetos: Windows
req.typenames: IMAGE_FUNCTION_ENTRY64, *PIMAGE_FUNCTION_ENTRY64
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAGE_FUNCTION_ENTRY64
 - winnt/_IMAGE_FUNCTION_ENTRY64
 - PIMAGE_FUNCTION_ENTRY64
 - winnt/PIMAGE_FUNCTION_ENTRY64
 - IMAGE_FUNCTION_ENTRY64
 - winnt/IMAGE_FUNCTION_ENTRY64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - IMAGE_FUNCTION_ENTRY
---

# IMAGE_FUNCTION_ENTRY64 structure


## -description

Represents an entry in the function table.

## -struct-fields

### -field StartingAddress

The image address of the start of the function.

### -field EndingAddress

The image address of the end of the function.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.EndOfPrologue

The image address of the end of the prologue code.

### -field DUMMYUNIONNAME.UnwindInfoAddress

## -remarks

The following definition exists for 64-bit support.


```cpp
typedef struct _IMAGE_FUNCTION_ENTRY64 {
    ULONGLONG   StartingAddress;
    ULONGLONG   EndingAddress;
    union {
        ULONGLONG   EndOfPrologue;
        ULONGLONG   UnwindInfoAddress;
    };
} IMAGE_FUNCTION_ENTRY64, *PIMAGE_FUNCTION_ENTRY64;
```

## -see-also

<a href="/windows/desktop/Debug/imagehlp-structures">ImageHlp Structures</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-stackframe">STACKFRAME64</a>
