---
UID: NF:clfsw32.CloseAndResetLogFile
title: CloseAndResetLogFile function
author: windows-sdk-content
description: Resets the log file and then shuts the log.
old-location: fs\closeandresetlogfile.htm
tech.root: Clfs
ms.assetid: 333b2de0-f472-43f7-ae57-5cefa7ab6746
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CloseAndResetLogFile, CloseAndResetLogFile function [Files], clfsw32/CloseAndResetLogFile, fs.closeandresetlogfile
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
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - CloseAndResetLogFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseAndResetLogFile function


## -description


Resets the log file and then shuts the log.  This nullifies any client restart areas and resets the base log sequence number (LSN) for the log.   You do not need to close a log stream handle after calling this function.   


## -parameters




### -param hLog [in]

A handle to a dedicated or multiplexed log. 

This handle is returned by a successful call to <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>.  It is invalidated on successful completion of the call. No other operations that use this handle, or a derivative of this handle, can be called after this function has returned.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following  list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>
 

 

