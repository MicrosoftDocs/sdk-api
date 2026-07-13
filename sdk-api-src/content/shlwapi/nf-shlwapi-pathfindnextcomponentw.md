---
UID: NF:shlwapi.PathFindNextComponentW
title: PathFindNextComponentW function (shlwapi.h)
description: Parses a path and returns the portion of that path that follows the first backslash. (Unicode)
helpviewer_keywords: ["PathFindNextComponent", "PathFindNextComponent function [Windows Shell]", "PathFindNextComponentW", "_win32_PathFindNextComponent", "shell.PathFindNextComponent", "shlwapi/PathFindNextComponent", "shlwapi/PathFindNextComponentW"]
old-location: shell\PathFindNextComponent.htm
tech.root: shell
ms.assetid: 2c76b901-dc0e-4f26-93c8-3c59b8f7147d
ms.date: 12/05/2018
ms.keywords: PathFindNextComponent, PathFindNextComponent function [Windows Shell], PathFindNextComponentA, PathFindNextComponentW, _win32_PathFindNextComponent, shell.PathFindNextComponent, shlwapi/PathFindNextComponent, shlwapi/PathFindNextComponentA, shlwapi/PathFindNextComponentW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathFindNextComponentW (Unicode) and PathFindNextComponentA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathFindNextComponentW
 - shlwapi/PathFindNextComponentW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathFindNextComponent
 - PathFindNextComponentA
 - PathFindNextComponentW
---

# PathFindNextComponentW function


## -description

Parses a path and returns the portion of that path that follows the first backslash.

## -parameters

### -param pszPath [in]

Type: <b>PTSTR</b>

A pointer to a null-terminated string that contains the path to parse. This string must not be longer than MAX_PATH characters, plus the terminating null character. Path components are delimited by backslashes. For instance, the path "c:\path1\path2\file.txt" has four components: c:, path1, path2, and file.txt.

## -returns

Type: <b>PTSTR</b>

Returns a pointer to a null-terminated string that contains the truncated path.

If <i>pszPath</i> points to the last component in the path, this function returns a pointer to the terminating null character.

If <i>pszPath</i> points to the terminating null character or if the call fails, this function returns <b>NULL</b>.

## -remarks

<b>PathFindNextComponent</b>  walks a path string until it encounters a backslash ("\\"), ignores everything up to that point including the backslash, and returns the rest of the path. Therefore, if a path begins with a backslash (such as \path1\path2), the function simply removes the initial backslash and returns the rest (path1\path2).


#### Examples

The following simple console application passes various strings to <b>PathFindNextComponent</b> to demonstrate what the function recognizes as a path component and to show what is returned. To run this code in Visual Studio, you must link to Shlwapi.lib and define UNICODE in the preprocessor commands in the project settings.


```cpp

#include <windows.h>
#include <iostream>
#include <shlwapi.h>

#pragma comment(lib, "shlwapi.lib")     // Link to this file.

int main()
{
    using namespace std;
   
    PCWSTR path = L"c:\\path1\\path2\\file.txt";
 
    // This loop passes a full path to PathFindNextComponent and feeds the 
    // results of that call back into the function until the entire path has
    // been walked.
    while (path)
    {
        PCWSTR oldPath = path;
        path = PathFindNextComponent(path);
 
        // The path variable pointed to the terminating null character.
        if (path == NULL)
        {
            wcout << L"The terminating null character returns NULL\n\n";
        }
        // The path variable pointed to a path with only one component.
		else if (*path == 0)
        {
            wcout << L"The path " << oldPath 
                  << L" returns a pointer to the terminating null character\n"; 
        }
        else 
        {
            wcout << L"The path " << oldPath << L" returns " << path << L"\n";
        }
    }
 
    // These calls demonstrate the results of different path forms.
    // Note that where those paths begin with backslashes, those
    // backslashes are merely stripped away and the entire path is returned.

    PCWSTR path1 = L"\\path1";

    wcout << L"The path " << path1 << L" returns " 
          << PathFindNextComponent(path1);
        
    PCWSTR path2 = L"\\path1\\path2";

    wcout << L"\nThe path " << path2 << L" returns "
          << PathFindNextComponent(path2);
        
    PCWSTR path3 = L"path1\\path2";
 
    wcout << L"\nThe path " << path3 << L" returns "
          << PathFindNextComponent(path3);
 
    wcout << L"\nThe path " << L"c:\\file.txt" << L" returns "
          << PathFindNextComponent(L"c:\\file.txt");
 
    return 0;
}

OUTPUT:
===========
The path c:\path1\path2\file.txt returns path1\path2\file.txt
The path path1\path2\file.txt returns path2\file.txt
The path path2\file.txt returns file.txt
The path file.txt returns a pointer to the terminating null character
The terminating null character returns NULL

The path \path1 returns path1
The path \path1\path2 returns path1\path2
The path path1\path2 returns path2
The path c:\file.txt returns file.txt
```





> [!NOTE]
> The shlwapi.h header defines PathFindNextComponent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

