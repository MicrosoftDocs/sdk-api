---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# HANDLE_OPTIONS enumeration


## -description


Defines the flags of the file handle.


## -enum-fields




### -field HO_NONE

None.


### -field HO_OPEN_REQUIRING_OPLOCK

This value is for internal use only.


### -field HO_DELETE_ON_CLOSE

The file is to be deleted immediately after this handle is closed.



### -field HO_SEQUENTIAL_SCAN

Access is intended to be sequential from beginning to end. The system can use this as a hint to optimize file caching.
For additional information, see <a href="https://msdn.microsoft.com/library/windows/desktop/aa363858(v=vs.85).aspx">Caching Behavior</a>.


### -field HO_RANDOM_ACCESS

Access is intended to be random. The system can use this as a hint to optimize file caching.
For more information, see  <a href="https://msdn.microsoft.com/library/windows/desktop/aa363858(v=vs.85).aspx">Caching Behavior</a>.


### -field HO_NO_BUFFERING

The file is being opened with no system caching for data reads and writes. This flag does not affect hard disk caching or memory mapped files.
There are strict requirements for successfully working with files opened with this flag. For details see  <a href="https://msdn.microsoft.com/library/windows/desktop/cc644950(v=vs.85).aspx">File Buffering</a>.


### -field HO_OVERLAPPED

The file is being opened or created for asynchronous I/O.
For information about considerations when using a file handle created with this flag, see  <a href="https://msdn.microsoft.com/library/windows/desktop/aa363858(v=vs.85).aspx">Synchronous and Asynchronous I/O Handles</a>.


### -field HO_WRITE_THROUGH

Write operations will not go through any intermediate cache, they will go directly to disk.
For additional information, see  <a href="https://msdn.microsoft.com/library/windows/desktop/aa363858(v=vs.85).aspx">Caching Behavior</a>.


