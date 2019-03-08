---
UID: NF:errhandlingapi.GetLastError
title: GetLastError function
author: windows-sdk-content
description: Retrieves the calling thread's last-error code value.
old-location: base\getlasterror.htm
tech.root: Debug
ms.assetid: d852e148-985c-416f-a5a7-27b6914b45d4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLastError, GetLastError function, _win32_getlasterror, base.getlasterror, errhandlingapi/GetLastError
ms.topic: function
req.header: errhandlingapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-errorhandling-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-errorhandling-l1-1-1.dll
 - API-MS-Win-Core-errorhandling-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ErrorHandling-L1-1-3.dll
api_name:
 - GetLastError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetLastError function


## -description


Retrieves the calling thread's last-error code value. The last-error code is maintained on a per-thread basis. Multiple threads do not overwrite each other's last-error code.

<b>Visual Basic:  </b>Applications should call <b>err.LastDllError</b> instead of 
<b>GetLastError</b>.


## -parameters






## -returns



The return value is the calling thread's last-error code.

The Return Value section of the documentation for each function that sets the last-error code notes the conditions under which the function sets the last-error code. Most functions that set the thread's last-error code set it when they fail. However, some functions also set the last-error code when they succeed. If the function is not documented to set the last-error code, the value returned by this function is simply the most recent last-error code to have been set; some functions set the last-error code to 0 on success and others do not.




## -remarks



Functions executed by the calling thread set this value by calling the 
<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> function. You should call the 
<b>GetLastError</b> function immediately when a function's return value indicates that such a call will return useful data. That is because some functions call 
<b>SetLastError</b> with a zero when they succeed, wiping out the error code set by the most recently failed function.

To obtain an error string for system error codes, use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function. For a complete list of error codes provided by the operating system, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.

The error codes returned by a function are not part of the Windows API specification and can vary by operating system or device driver. For this reason, we cannot provide the complete list of error codes that can be returned by each function. There are also many functions whose documentation does not include even a partial list of error codes that can be returned.

Error codes are 32-bit values (bit 31 is the most significant bit). Bit 29 is reserved for application-defined error codes; no system error code has this bit set. If you are defining an error code for your application, set this bit to one. That indicates that the error code has been defined by an application, and ensures that your error code does not conflict with any error codes defined by the system.

To convert a system error into an <b>HRESULT</b> value, use the 
<a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/4cc626ac-7574-44ce-8377-e0bdd8e74b7e">Retrieving the Last-Error Code</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5">Error Handling Functions</a>



<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a>



<a href="https://msdn.microsoft.com/fd5b0d6e-78cf-4f51-b61d-d32576cd485a">Last-Error Code</a>



<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a>



<a href="https://msdn.microsoft.com/d97494db-868a-49d4-a613-e8beba86d4e6">SetLastErrorEx</a>
 

 

