---
UID: NS:winbase._FILE_IO_PRIORITY_HINT_INFO
title: FILE_IO_PRIORITY_HINT_INFO
author: windows-sdk-content
description: Specifies the priority hint for a file I/O operation.
old-location: fs\file_io_priority_hint_info.htm
tech.root: fileio
ms.assetid: a142b8fd-b71c-4449-a8c6-fb23715d1576
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PFILE_IO_PRIORITY_HINT_INFO, FILE_IO_PRIORITY_HINT_INFO, FILE_IO_PRIORITY_HINT_INFO structure [Files], PFILE_IO_PRIORITY_HINT_INFO, PFILE_IO_PRIORITY_HINT_INFO structure pointer [Files], _FILE_IO_PRIORITY_HINT_INFO, fs.file_io_priority_hint_info, winbase/FILE_IO_PRIORITY_HINT_INFO, winbase/PFILE_IO_PRIORITY_HINT_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - WinBase.h
api_name:
 - FILE_IO_PRIORITY_HINT_INFO
product: Windows
targetos: Windows
req.typenames: FILE_IO_PRIORITY_HINT_INFO, *PFILE_IO_PRIORITY_HINT_INFO
req.redist: 
---

# FILE_IO_PRIORITY_HINT_INFO structure


## -description


Specifies the priority hint for a file I/O operation.


## -struct-fields




### -field PriorityHint

The priority hint. This member is a value from the 
      <a href="https://msdn.microsoft.com/768e563a-5ff5-4dd2-8811-0a823c253a31">PRIORITY_HINT</a> enumeration.


## -remarks



The <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a> function 
    can be used with this structure to associate a priority hint with I/O operations on a file-handle basis. In 
    addition to the idle priority (very low), this function allows normal priority and low priority. Whether these 
    priorities are supported and honored by the underlying drivers depends on their implementation (which is why they 
    are called hints). For more information, see the 
    <a href="Http://go.microsoft.com/fwlink/p/?linkid=98562">I/O Prioritization in Windows Vista</a> 
    white paper on the Windows Hardware Developer Central (WHDC) website.

This structure must be aligned on a <b>LONGLONG</b> (8-byte) boundary.




## -see-also




<a href="https://msdn.microsoft.com/768e563a-5ff5-4dd2-8811-0a823c253a31">PRIORITY_HINT</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 

