---
UID: NF:appmodel.PackageFamilyNameFromFullName
title: PackageFamilyNameFromFullName function
author: windows-sdk-content
description: Gets the package family name for the specified package full name.
old-location: appxpkg\packagefamilynamefromfullname.htm
old-project: appxpkg
ms.assetid: 98E95CE5-E970-4A19-BAD3-994DAEC4BEA0
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: PackageFamilyNameFromFullName, PackageFamilyNameFromFullName function [App packaging and management], appmodel/PackageFamilyNameFromFullName, appxpkg.packagefamilynamefromfullname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: appmodel.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: PackageOrigin
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-AppModel-Runtime-l1-1-0.dll
 - kernel32legacy.dll
 - Ext-MS-Win-kernel32-package-l1-1-0.dll
 - Kernel.AppCore.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - Ext-MS-Win-Kernel32-package-l1-1-2.dll
 - ext-ms-win-kernel32-package-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - PackageFamilyNameFromFullName
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# PackageFamilyNameFromFullName function


## -description


Gets the package family name for the specified package full name.


## -parameters




### -param packageFullName [in]

Type: <b>PCWSTR</b>

The full name of a package.


### -param packageFamilyNameLength [in, out]

Type: <b>UINT32*</b>

On input, the size of the <i>packageFamilyName</i> buffer, in characters. On output, the size of the package family name returned, in characters, including the null terminator.


### -param packageFamilyName [out, optional]

Type: <b>PWSTR</b>

The package family name.


## -returns



Type: <b>LONG</b>

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function returns an error code. The possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to hold the data. The required size is specified  by <i>packageFamilyNameLength</i>.

</td>
</tr>
</table>
 




## -remarks



For info about string size limits, see <a href="https://msdn.microsoft.com/C4F81822-B502-4360-AEA4-829F1AB926BF">Identity constants</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define _UNICODE 1
#define UNICODE 1

#include &lt;Windows.h&gt;
#include &lt;appmodel.h&gt;
#include &lt;malloc.h&gt;
#include &lt;stdio.h&gt;

int ShowUsage();
void FullNameToFamilyName(__in PCWSTR fullName);

int ShowUsage()
{
    wprintf(L"Usage: PackageFamilyNameFromFullName &lt;fullname&gt; [&lt;fullname&gt;...]\n");
    return 1;
}

int __cdecl wmain(__in int argc, __in_ecount(argc) WCHAR * argv[])
{
    if (argc &lt;= 1)
        return ShowUsage();

    for (int i=1; i&lt;argc; ++i)
        FullNameToFamilyName(argv[i]);

    return 0;
}

void FullNameToFamilyName(__in PCWSTR fullName)
{
    wprintf(L"FullName: %s\n", fullName);
    UINT32 length = 0;
    LONG rc = PackageFamilyNameFromFullName(fullName, &amp;length, NULL);
    if (rc == ERROR_SUCCESS)
    {
        wprintf(L"PackageFamilyNameFromFullName unexpectedly succeeded\n");
        return;
    }
    else if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        wprintf(L"Error %d in PackageFamilyNameFromFullName\n", rc);
        return;
    }

    PWSTR familyName = (PWSTR) malloc(length * sizeof(WCHAR));
    if (familyName == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return;
    }

    rc = PackageFamilyNameFromFullName(fullName, &amp;length, familyName);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d converting PackageFamilyName to FullName\n", rc);
    else
        wprintf(L"Package Family Name = %s\n", familyName);

    free(familyName);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/39DBFBDD-A1CC-45C3-A5DD-5ED9697F9AFE">GetCurrentPackageFamilyName</a>



<a href="https://msdn.microsoft.com/AC239898-9924-4193-9072-7A7EEC2D03E9">GetPackageFamilyName</a>



<a href="https://msdn.microsoft.com/198DAB6B-21D2-4ACB-87DF-B3F4EFBEE323">PackageFamilyNameFromId</a>



<a href="https://msdn.microsoft.com/0024AF55-295E-49B1-90C2-9144D336529B">PackageFullNameFromId</a>



<a href="https://msdn.microsoft.com/EED832F8-E4F7-4A0F-93E2-451F78F67767">PackageIdFromFullName</a>



<a href="https://msdn.microsoft.com/4AA5BD75-F865-40D6-9C10-E54C197D47C4">PackageNameAndPublisherIdFromFamilyName</a>
 

 

