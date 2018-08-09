---
UID: NF:appmodel.PackageFamilyNameFromId
title: PackageFamilyNameFromId function
author: windows-sdk-content
description: Gets the package family name for the specified package identifier.
old-location: appxpkg\packagefamilynamefromid.htm
old-project: appxpkg
ms.assetid: 198DAB6B-21D2-4ACB-87DF-B3F4EFBEE323
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: PackageFamilyNameFromId, PackageFamilyNameFromId function [App packaging and management], appmodel/PackageFamilyNameFromId, appxpkg.packagefamilynamefromid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: appmodel.h
req.include-header: 
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
 - PackageFamilyNameFromId
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# PackageFamilyNameFromId function


## -description


Gets the package family name for the specified package identifier.


## -parameters




### -param packageId [in]

Type: <b>const <a href="https://msdn.microsoft.com/4B15281A-2227-47B7-A750-0A01DB8543FC">PACKAGE_ID</a>*</b>

The package identifier.


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
#include &lt;stdlib.h&gt;
#include &lt;errno.h&gt;
#include &lt;stdio.h&gt;

int ShowUsage();
bool ParseArchitecture(__in PCWSTR architectureString, __out UINT32 * architecture);
bool ParseVersion(__in PCWSTR versionString, __out PACKAGE_VERSION * version);

int ShowUsage()
{
    wprintf(L"Usage: PackageFamilyNameFromId &lt;name&gt;&lt;version&gt; &lt;arch&gt; &lt;resourceid&gt; &lt;publisher&gt;\n");
    return 1;
}

int __cdecl wmain(__in int argc, __in_ecount(argc) WCHAR * argv[])
{
    if (argc &lt;= 5)
        return ShowUsage();

    PACKAGE_ID packageId;
    ZeroMemory(&amp;packageId, sizeof(packageId));
    packageId.name = argv[1];
    if (!ParseVersion(argv[2], &amp;packageId.version))
        return 2;
    if (!ParseArchitecture(argv[3], &amp;packageId.processorArchitecture))
        return 3;
    packageId.resourceId = argv[4];
    packageId.publisher = argv[5];

    UINT32 length = 0;
    LONG rc = PackageFamilyNameFromId(&amp;packageId, &amp;length, NULL);
    if (rc == ERROR_SUCCESS)
    {
        wprintf(L"PackageFamilyNameFromId unexpected succeeded\n");
        return 4;
    }
    else if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        wprintf(L"Error %d in PackageFamilyNameFromId\n", rc);
        return 5;
    }

    PWSTR familyName = (PWSTR) malloc(length * sizeof(WCHAR));
    if (familyName == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return 6;
    }

    rc = PackageFamilyNameFromId(&amp;packageId, &amp;length, familyName);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d converting Package Id to Family Name\n", rc);
    else
        wprintf(L"Package Family Name = %s\n", familyName);

    free(familyName);

    return rc == ERROR_SUCCESS ? 0 : 7;
}

bool ParseArchitecture(__in PCWSTR architectureString, __out UINT32 * architecture)
{
    if (_wcsicmp(architectureString, L"neutral") == 0)
        *architecture = PROCESSOR_ARCHITECTURE_NEUTRAL;
    else if (_wcsicmp(architectureString, L"x86") == 0)
        *architecture = PROCESSOR_ARCHITECTURE_INTEL;
    else if (_wcsicmp(architectureString, L"x64") == 0)
        *architecture = PROCESSOR_ARCHITECTURE_AMD64;
    else if (_wcsicmp(architectureString, L"arm") == 0)
        *architecture = PROCESSOR_ARCHITECTURE_ARM;
    else
    {
        wprintf(L"Invalid architecture\n");
        return false;
    }
    return true;
}

bool ParseVersion(__in PCWSTR versionString, __out PACKAGE_VERSION * version)
{
    PWSTR s = (PWSTR) versionString;

    ULONG n = wcstoul(s, &amp;s, 10);
    if (((n == 0) || (n &gt; 65535)) &amp;&amp; (errno == ERANGE)) {
        wprintf(L"Invalid Version (Major)\n");
        return false;
    }
    version-&gt;Major = (USHORT) n;

    if (*s != L'.')
    {
        wprintf(L"Invalid Version\n");
        return false;
    }

    n = wcstoul(++s, &amp;s, 10);
    if (((n == 0) || (n &gt; 65535)) &amp;&amp; (errno == ERANGE)) {
        wprintf(L"Invalid Version (Minor)\n");
        return false;
    }
    version-&gt;Minor = (USHORT) n;

    if (*s != L'.')
    {
        wprintf(L"Invalid Version\n");
        return false;
    }

    n = wcstoul(++s, &amp;s, 10);
    if (((n == 0) || (n &gt; 65535)) &amp;&amp; (errno == ERANGE)) {
        wprintf(L"Invalid Version (Build)\n");
        return false;
    }
    version-&gt;Build = (USHORT) n;

    if (*s != L'.')
    {
        wprintf(L"Invalid Version\n");
        return false;
    }

    n = wcstoul(++s, &amp;s, 10);
    if (((n == 0) || (n &gt; 65535)) &amp;&amp; (errno == ERANGE)) {
        wprintf(L"Invalid Version (Revision)\n");
        return false;
    }
    version-&gt;Revision = (USHORT) n;

    return true;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/39DBFBDD-A1CC-45C3-A5DD-5ED9697F9AFE">GetCurrentPackageFamilyName</a>



<a href="https://msdn.microsoft.com/AC239898-9924-4193-9072-7A7EEC2D03E9">GetPackageFamilyName</a>



<a href="https://msdn.microsoft.com/98E95CE5-E970-4A19-BAD3-994DAEC4BEA0">PackageFamilyNameFromFullName</a>



<a href="https://msdn.microsoft.com/0024AF55-295E-49B1-90C2-9144D336529B">PackageFullNameFromId</a>



<a href="https://msdn.microsoft.com/EED832F8-E4F7-4A0F-93E2-451F78F67767">PackageIdFromFullName</a>



<a href="https://msdn.microsoft.com/4AA5BD75-F865-40D6-9C10-E54C197D47C4">PackageNameAndPublisherIdFromFamilyName</a>
 

 

