---
UID: NF:winuser.LoadStringW
title: LoadStringW function (winuser.h)
author: windows-sdk-content
description: Loads a string resource from the executable file associated with a specified module, copies the string into a buffer, and appends a terminating null character.
old-location: menurc\loadstring.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\loadstring.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LoadString, LoadString function [Menus and Other Resources], LoadStringA, LoadStringW, _win32_LoadString, _win32_loadstring_cpp, menurc.loadstring, winui._win32_loadstring, winuser/LoadString, winuser/LoadStringA, winuser/LoadStringW
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadStringW (Unicode) and LoadStringA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - API-MS-Win-Core-Stringloader-l1-1-0.dll
 - API-MS-Win-Core-Stringloader-l1-1-1.dll
 - API-MS-Win-DownLevel-user32-l1-1-1.dll
 - MinKernelBase.dll
 - kernel32.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - LoadString
 - LoadStringA
 - LoadStringW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LoadStringW function


## -description


Loads a string resource from the executable file associated with a specified module and either copies the string into a buffer with a terminating null character or returns a read-only pointer to the string resource itself.


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to an instance of the module whose executable file contains the string resource. To get the handle to the application itself, call the <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> function with <b>NULL</b>.


### -param uID [in]

Type: <b>UINT</b>

The identifier of the string to be loaded.


### -param lpBuffer [out]

Type: <b>LPTSTR</b>

The buffer to receive the string (if *cchBufferMax* is non-zero) or a read-only pointer to the string resource itself (if *cchBufferMax* is zero). Must be of sufficient length to hold a pointer (8 bytes). 


### -param cchBufferMax [in]

Type: <b>int</b>

The size of the buffer, in characters. The string is truncated and null-terminated if it is longer than the number of characters specified. If this parameter is 0, then <i>lpBuffer</i> receives a read-only pointer to the string resource itself.


## -returns



Type: <b>int</b>

If the function succeeds, the return value is one of the following:

- The number of characters copied into the buffer (if *cchBufferMax* is non-zero), not including the terminating null character.
- The number of characters in the string resource that *lpBuffer* points to (if *cchBufferMax* is zero). The string resource is not guaranteed to be null-terminated in the module's resource table, and you can use this value to determine where the string resource ends.
- Zero if the string resource does not exist. 
 
To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


## -remarks

If you pass 0 to *cchBufferMax* to return a read-only pointer to the string resource in the *lpBuffer* parameter, use the number of characters in the return value to determine the length of the string resource. String resources are not guaranteed to be null-terminated in the module's resource table. However, resource tables can contain null characters. String resources are stored in blocks of 16 strings, and any empty slots within a block are indicated by null characters. 

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
Using this function incorrectly can compromise the security of your application. Incorrect use includes specifying the wrong size in the <i>nBufferMax</i> parameter. For example, if <i>lpBuffer</i> points to a buffer <i>szBuffer</i> which is declared as <code>TCHAR szBuffer[100]</code>, then sizeof(szBuffer) gives the size of the buffer in bytes, which could lead to a buffer overflow for the Unicode version of the function. Buffer overflow situations are the cause of many security problems in applications. In this case, using <code>sizeof(szBuffer)/sizeof(TCHAR)</code> or <code>sizeof(szBuffer)/sizeof(szBuffer[0])</code> would give the proper size of the buffer.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms644909(v=VS.85).aspx">Creating a Child Window</a>

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646370(v=VS.85).aspx">LoadAccelerators</a>



<a href="https://msdn.microsoft.com/5eed5f78-deaf-4b23-986e-4802dc05936c">LoadBitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648391(v=VS.85).aspx">LoadCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648072(v=VS.85).aspx">LoadIcon</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647990(v=VS.85).aspx">LoadMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647991(v=VS.85).aspx">LoadMenuIndirect</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646979(v=VS.85).aspx">Strings</a>
 

 

