---
UID: NF:shellapi.CommandLineToArgvW
title: CommandLineToArgvW function (shellapi.h)
description: Parses a Unicode command line string and returns an array of pointers to the command line arguments, along with a count of such arguments, in a way that is similar to the standard C run-time argv and argc values.
helpviewer_keywords: ["CommandLineToArgvW","CommandLineToArgvW function [Windows Shell]","_shell_CommandLineToArgvW","shell.CommandLineToArgvW","shellapi/CommandLineToArgvW"]
old-location: shell\CommandLineToArgvW.htm
tech.root: shell
ms.assetid: 9889a016-b7a5-402b-8305-6f7c199d41b3
ms.date: 12/05/2018
ms.keywords: CommandLineToArgvW, CommandLineToArgvW function [Windows Shell], _shell_CommandLineToArgvW, shell.CommandLineToArgvW, shellapi/CommandLineToArgvW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CommandLineToArgvW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CommandLineToArgvW
 - shellapi/CommandLineToArgvW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-commandlinetoargv-l1-1-0.dll
 - Shell32.dll
 - API-MS-Win-DownLevel-shell32-l1-1-0.dll
 - ShCore.dll
 - API-MS-Win-ShCore-Obsolete-l1-1-0.dll
api_name:
 - CommandLineToArgvW
 - CommandLineToArgvW
---

# CommandLineToArgvW function


## -description

Parses a Unicode command line string and returns an array of pointers to the command line arguments, along with a count of such arguments, in a way that is similar to the standard C run-time <i>argv</i> and <i>argc</i> values.

## -parameters

### -param lpCmdLine [in]

Type: <b>LPCWSTR</b>

Pointer to a <b>null</b>-terminated Unicode string that contains the full command line. If this parameter is an empty string the function returns the path to the current executable file.

### -param pNumArgs [out]

Type: <b>int*</b>

Pointer to an <b>int</b> that receives the number of array elements returned, similar to <i>argc</i>.

## -returns

Type: <b>LPWSTR*</b>

A pointer to an array of <b>LPWSTR</b> values, similar to <i>argv</i>.

                    

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The address returned by <b>CommandLineToArgvW</b> is the address of the first element in an array of <b>LPWSTR</b> values; the number of pointers in this array is indicated by <i>pNumArgs</i>. Each pointer to a <b>null</b>-terminated Unicode string represents an individual argument found on the command line.

<b>CommandLineToArgvW</b> allocates a block of contiguous memory for pointers to the argument strings, and for the argument strings themselves; the calling application must free the memory used by the argument list when it is no longer needed. To free the memory, use a single call to the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

For more information about the <i>argv</i> and <i>argc</i> argument convention, see <a href="/previous-versions/88w63h9k(v=vs.85)">Argument Definitions</a> and <a href="/cpp/c-language/parsing-c-command-line-arguments">Parsing C Command-Line Arguments</a>.

The <a href="/windows/desktop/api/processenv/nf-processenv-getcommandlinew">GetCommandLineW</a> function can be used to get a command line string that is suitable for use as the <i>lpCmdLine</i> parameter.

This function accepts command lines that contain a program name; the program name can be enclosed in quotation marks or not.

<b>CommandLineToArgvW</b> has a special interpretation of backslash characters when they are followed by a quotation mark character ("). This interpretation assumes that any preceding argument is a valid file system path, or else it may behave unpredictably. 

This special interpretation controls the "in quotes" mode tracked by the parser. When this mode is off, whitespace terminates the current argument. When on, whitespace is added to the argument like all other characters.
    
                

<ul>
<li>2<i>n</i> backslashes followed by a quotation mark produce <i>n</i> backslashes followed by begin/end quote. This does not become part of the parsed argument, but toggles the "in quotes" mode.</li>
<li>(2<i>n</i>) + 1 backslashes followed by a quotation mark again produce <i>n</i> backslashes followed by a quotation mark literal ("). This does not toggle the "in quotes" mode.</li>
<li><i>n</i> backslashes not followed by a quotation mark simply produce <i>n</i> backslashes.</li>
</ul>
<div class="alert"><b>Important</b>  <p class="note"><b>CommandLineToArgvW</b> treats whitespace outside of quotation marks as argument delimiters. However, if <i>lpCmdLine</i> starts with any amount of whitespace, <b>CommandLineToArgvW</b> will consider the first argument to be an empty string. Excess whitespace at the end of <i>lpCmdLine</i> is ignored.

</div>
<div> </div>

#### Examples



The following example demonstrates how to parse a Unicode command-line string. The code frees the memory for the argument list at exit.


```cpp
#include <windows.h>
#include <stdio.h>
#include <shellapi.h>

int __cdecl main()
{
   LPWSTR *szArglist;
   int nArgs;
   int i;

   szArglist = CommandLineToArgvW(GetCommandLineW(), &nArgs);
   if( NULL == szArglist )
   {
      wprintf(L"CommandLineToArgvW failed\n");
      return 0;
   }
   else for( i=0; i<nArgs; i++) printf("%d: %ws\n", i, szArglist[i]);

// Free memory allocated for CommandLineToArgvW arguments.

   LocalFree(szArglist);

   return(1);
}
```
