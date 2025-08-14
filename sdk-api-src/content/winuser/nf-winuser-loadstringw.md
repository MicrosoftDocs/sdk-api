---
UID: NF:winuser.LoadStringW
title: LoadStringW function (winuser.h)
description: Loads a string resource from the executable file associated with a specified module, copies the string into a buffer, and appends a terminating null character. (Unicode)
helpviewer_keywords: ["LoadString", "LoadString function [Menus and Other Resources]", "LoadStringW", "_win32_LoadString", "_win32_loadstring_cpp", "menurc.loadstring", "winui._win32_loadstring", "winuser/LoadString", "winuser/LoadStringW"]
old-location: menurc\loadstring.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\loadstring.htm
ms.date: 12/05/2018
ms.keywords: LoadString, LoadString function [Menus and Other Resources], LoadStringA, LoadStringW, _win32_LoadString, _win32_loadstring_cpp, menurc.loadstring, winui._win32_loadstring, winuser/LoadString, winuser/LoadStringA, winuser/LoadStringW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LoadStringW
 - winuser/LoadStringW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-user32-l1-1-0.dll
 - api-ms-win-core-libraryloader-l1-2-3.dll
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
---

# LoadStringW function


## -description

Loads a string resource from the executable file associated with a specified module and either copies the string into a buffer with a terminating null character or returns a read-only pointer to the string resource itself.

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to an instance of the module whose executable file contains the string resource. To get the handle to the application itself, call the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a> function with <b>NULL</b>.

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
 
To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If you pass 0 to *cchBufferMax* to return a read-only pointer to the string resource in the *lpBuffer* parameter, use the number of characters in the return value to determine the length of the string resource. String resources are not guaranteed to be null-terminated in the module's resource table. However, resource tables can contain null characters. String resources are stored in blocks of 16 strings, and any empty slots within a block are indicated by null characters. 

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
Using this function incorrectly can compromise the security of your application. Incorrect use includes specifying the wrong size in the <i>nBufferMax</i> parameter. For example, if <i>lpBuffer</i> points to a buffer <i>szBuffer</i> which is declared as <code>TCHAR szBuffer[100]</code>, then sizeof(szBuffer) gives the size of the buffer in bytes, which could lead to a buffer overflow for the Unicode version of the function. Buffer overflow situations are the cause of many security problems in applications. In this case, using <code>sizeof(szBuffer)/sizeof(TCHAR)</code> or <code>sizeof(szBuffer)/sizeof(szBuffer[0])</code> would give the proper size of the buffer.


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-the-multiple-document-interface">Creating a Child Window</a>

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines LoadString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa">LoadAccelerators</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadbitmapa">LoadBitmap</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadmenua">LoadMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadmenuindirecta">LoadMenuIndirect</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/menurc/strings">Strings</a>
