---
UID: NS:winnt._FILE_SEGMENT_ELEMENT
title: "_FILE_SEGMENT_ELEMENT"
author: windows-sdk-content
description: Union that contains a 64-bit value that points to a page of data.
old-location: fs\file_segment_element.htm
old-project: FileIO
ms.assetid: dde79dcb-95ec-4a9e-87a4-9ad99ac6266e
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PFILE_SEGMENT_ELEMENT, FILE_SEGMENT_ELEMENT, FILE_SEGMENT_ELEMENT union [Files], PFILE_SEGMENT_ELEMENT, PFILE_SEGMENT_ELEMENT union pointer [Files], _FILE_SEGMENT_ELEMENT, fs.file_segment_element, winnt/FILE_SEGMENT_ELEMENT, winnt/PFILE_SEGMENT_ELEMENT"
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
req.typenames: FILE_SEGMENT_ELEMENT, *PFILE_SEGMENT_ELEMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinNT.h
api_name:
-	FILE_SEGMENT_ELEMENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _FILE_SEGMENT_ELEMENT structure


## -description


Union that contains a 64-bit value that points to a page of data. This is used by 
    the <a href="https://msdn.microsoft.com/4ed7c47b-d40b-4016-8550-0af17ee9e86d">ReadFileScatter</a> and 
    <a href="https://msdn.microsoft.com/9590eabb-6e85-406e-8101-e67f87e6850b">WriteFileGather</a> functions.


## -struct-fields




### -field Buffer

<b>PVOID64</b> representation of 64-bit value.

Assigning a pointer to the <b>Buffer</b> member will sign-extend the value if the code is 
      compiled as 32-bits; this can break 32-bit large-address aware applications running on systems configured with 
      <a href="https://msdn.microsoft.com/991eb86f-9e6f-4084-8b6f-f979e42104b5">4-Gigabyte Tuning</a> or running under WOW64 on 64-bit 
      Windows. Therefore, use the <b>PtrToPtr64</b> macro when assigning pointers to the 
      <b>Buffer</b> member.


### -field Alignment

<b>ULONGLONG</b> representation of 64-bit value.


## -see-also




<a href="https://msdn.microsoft.com/406d5c0f-b49a-4075-ac3e-c5b55a0c3fe9">File Management Structures</a>



<a href="https://msdn.microsoft.com/4ed7c47b-d40b-4016-8550-0af17ee9e86d">ReadFileScatter</a>



<a href="https://msdn.microsoft.com/9590eabb-6e85-406e-8101-e67f87e6850b">WriteFileGather</a>
 

 

