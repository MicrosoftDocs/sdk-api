---
UID: NS:winnt._IMAGE_FUNCTION_ENTRY64
title: "_IMAGE_FUNCTION_ENTRY64"
author: windows-driver-content
description: Represents an entry in the function table.
old-location: base\image_function_entry_str.htm
old-project: Debug
ms.assetid: ced956ec-7a12-4548-8e38-a1c1057c05e8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PIMAGE_FUNCTION_ENTRY64, IMAGE_FUNCTION_ENTRY, IMAGE_FUNCTION_ENTRY structure, IMAGE_FUNCTION_ENTRY64, PIMAGE_FUNCTION_ENTRY, PIMAGE_FUNCTION_ENTRY structure pointer, _IMAGE_FUNCTION_ENTRY, _IMAGE_FUNCTION_ENTRY64, _win32_image_function_entry_str, base.image_function_entry_str, winnt/IMAGE_FUNCTION_ENTRY, winnt/PIMAGE_FUNCTION_ENTRY"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: IMAGE_FUNCTION_ENTRY64, *PIMAGE_FUNCTION_ENTRY64
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinNT.h
api_name:
-	IMAGE_FUNCTION_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _IMAGE_FUNCTION_ENTRY64 structure


## -description


Represents an entry in the function table.


## -struct-fields




### -field StartingAddress

The image address of the start of the function.


### -field EndingAddress

The image address of the end of the function.


### -field DUMMYUNIONNAME

 




#### - EndOfPrologue

The image address of the end of the prologue code.


## -remarks



The following definition exists for 64-bit support.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef struct _IMAGE_FUNCTION_ENTRY64 {
    ULONGLONG   StartingAddress;
    ULONGLONG   EndingAddress;
    union {
        ULONGLONG   EndOfPrologue;
        ULONGLONG   UnwindInfoAddress;
    };
} IMAGE_FUNCTION_ENTRY64, *PIMAGE_FUNCTION_ENTRY64;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b88c7a21-933f-450c-97e8-04cf3c5f9b11">ImageHlp Structures</a>



<a href="https://msdn.microsoft.com/2809e3f1-c64a-4753-9fca-f78e89a878b2">STACKFRAME64</a>
 

 

