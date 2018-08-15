---
UID: NF:winuser.SetLastErrorEx
title: SetLastErrorEx function
author: windows-sdk-content
description: Sets the last-error code.
old-location: base\setlasterrorex.htm
old-project: debug
ms.assetid: d97494db-868a-49d4-a613-e8beba86d4e6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetLastErrorEx, SetLastErrorEx function, _win32_setlasterrorex, base.setlasterrorex, winuser/SetLastErrorEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SetLastErrorEx
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetLastErrorEx function


## -description


Sets the last-error code.

Currently, this function is identical to the 
<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> function. The second parameter is ignored.


## -parameters




### -param dwErrCode [in]

The last-error code for the thread.


### -param dwType [in]

This parameter is ignored.


## -returns



This function does not return a value.




## -remarks



The last-error code is kept in thread local storage so that multiple threads do not overwrite each other's values.

Most functions call 
<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> or <b>SetLastErrorEx</b> only when they fail. However, some system functions call 
<b>SetLastError</b> or <b>SetLastErrorEx</b> under conditions of success; those cases are noted in each function's documentation.

Applications can optionally retrieve the value set by this function by using the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function immediately after a function fails.

Error codes are 32-bit values (bit 31 is the most significant bit). Bit 29 is reserved for application-defined error codes; no system error code has this bit set. If you are defining an error code for your application, set this bit to indicate that the error code has been defined by the application and to ensure that your error code does not conflict with any system-defined error codes.




## -see-also




<a href="https://msdn.microsoft.com/ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5">Error Handling Functions</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/fd5b0d6e-78cf-4f51-b61d-d32576cd485a">Last-Error Code</a>
 

 

