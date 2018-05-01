---
UID: NF:clfsw32.GetLogFileInformation
title: GetLogFileInformation function
author: windows-driver-content
description: Returns a buffer that contains metadata about a specified log and its current state, which is defined by the CLFS_INFORMATION structure.
old-location: fs\getlogfileinformation.htm
old-project: Clfs
ms.assetid: 29bb2f18-760d-4a38-8dce-85099da7f96c
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: GetLogFileInformation, GetLogFileInformation function [Files], clfsw32/GetLogFileInformation, fs.getlogfileinformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Clfsw32.dll
api_name:
-	GetLogFileInformation
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# GetLogFileInformation function


## -description


Returns a buffer that contains metadata about a specified log and its current state, which is defined by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff541790">CLFS_INFORMATION</a> structure.

Data that is obtained  reflects the state of the log only at the time when the call is made. Typically, a client can continue to cache and use fields from this structure until the next time that it appends records or writes its restart area. At that time, some of the information becomes stale.


## -parameters




### -param hLog [in]

A handle to an open log that is obtained from a successful call to <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>.  

The log handle can refer to a dedicated or multiplexed log.


### -param pinfoBuffer [in, out]

A pointer to a user-allocated <a href="https://msdn.microsoft.com/library/windows/hardware/ff541790">CLFS_INFORMATION</a> structure that receives the log metadata.


### -param cbBuffer [in, out]

A pointer to a variable that on input specifies the size, in bytes, of the metadata buffer pointed to by <i>pinfoBuffer</i>.

 On output, it specifies the number of bytes that are actually copied into <i>pinfoBuffer</i>.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

 The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/06f5919e-b98f-4502-9653-9ef42c1ebe5a">
        CLFS_INFORMATION</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>



<a href="https://msdn.microsoft.com/2e47a5c9-a0bd-4cd1-ba30-9ebde6df0f91">Obtaining the Next LSN</a>
 

 

