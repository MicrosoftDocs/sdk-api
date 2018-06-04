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

# PathFindNextComponentA function


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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#include &lt;windows.h&gt;
#include &lt;iostream&gt;
#include &lt;shlwapi.h&gt;

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
            wcout &lt;&lt; L"The terminating null character returns NULL\n\n";
        }
        // The path variable pointed to a path with only one component.
		else if (*path == 0)
        {
            wcout &lt;&lt; L"The path " &lt;&lt; oldPath 
                  &lt;&lt; L" returns a pointer to the terminating null character\n"; 
        }
        else 
        {
            wcout &lt;&lt; L"The path " &lt;&lt; oldPath &lt;&lt; L" returns " &lt;&lt; path &lt;&lt; L"\n";
        }
    }
 
    // These calls demonstrate the results of different path forms.
    // Note that where those paths begin with backslashes, those
    // backslashes are merely stripped away and the entire path is returned.

    PCWSTR path1 = L"\\path1";

    wcout &lt;&lt; L"The path " &lt;&lt; path1 &lt;&lt; L" returns " 
          &lt;&lt; PathFindNextComponent(path1);
        
    PCWSTR path2 = L"\\path1\\path2";

    wcout &lt;&lt; L"\nThe path " &lt;&lt; path2 &lt;&lt; L" returns "
          &lt;&lt; PathFindNextComponent(path2);
        
    PCWSTR path3 = L"path1\\path2";
 
    wcout &lt;&lt; L"\nThe path " &lt;&lt; path3 &lt;&lt; L" returns "
          &lt;&lt; PathFindNextComponent(path3);
 
    wcout &lt;&lt; L"\nThe path " &lt;&lt; L"c:\\file.txt" &lt;&lt; L" returns "
          &lt;&lt; PathFindNextComponent(L"c:\\file.txt");
 
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
The path c:\file.txt returns file.txt</pre>
</td>
</tr>
</table></span></div>


