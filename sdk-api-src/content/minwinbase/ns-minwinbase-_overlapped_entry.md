---
UID: NS:minwinbase._OVERLAPPED_ENTRY
title: "_OVERLAPPED_ENTRY"
author: windows-sdk-content
description: Contains the information returned by a call to the GetQueuedCompletionStatusEx function.
old-location: fs\overlapped_entry.htm
old-project: fileio
ms.assetid: 3e244e6c-0731-477a-b1d3-2601c29449ca
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPOVERLAPPED_ENTRY, LPOVERLAPPED_ENTRY, LPOVERLAPPED_ENTRY structure pointer [Files], OVERLAPPED_ENTRY, OVERLAPPED_ENTRY structure [Files], _OVERLAPPED_ENTRY, fs.overlapped_entry, minwinbase/LPOVERLAPPED_ENTRY, minwinbase/OVERLAPPED_ENTRY, winbase/LPOVERLAPPED_ENTRY, winbase/OVERLAPPED_ENTRY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minwinbase.h
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
tech.root: 
req.typenames: OVERLAPPED_ENTRY, *LPOVERLAPPED_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MinWinBase.h
 - WinBase.h
api_name:
 - OVERLAPPED_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _OVERLAPPED_ENTRY structure


## -description


Contains the information returned by a call to the 
    <a href="https://msdn.microsoft.com/3996c02c-562c-4697-a091-e241ad54b239">GetQueuedCompletionStatusEx</a> 
    function.


## -struct-fields




### -field lpCompletionKey

Receives the completion key value associated with the file handle whose I/O operation has completed. A 
      completion key is a per-file key that is specified in a call to 
      <a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a>.


### -field lpOverlapped

Receives the address of the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure 
      that was specified when the completed I/O operation was started.


### -field Internal

Reserved.


### -field dwNumberOfBytesTransferred

Receives the number of bytes transferred during the I/O operation that has completed.


## -see-also




<a href="https://msdn.microsoft.com/3996c02c-562c-4697-a091-e241ad54b239">GetQueuedCompletionStatusEx</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

