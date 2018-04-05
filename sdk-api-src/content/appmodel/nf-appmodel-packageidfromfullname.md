---
UID: NF:appmodel.PackageIdFromFullName
title: PackageIdFromFullName function
author: windows-driver-content
description: Gets the package identifier (ID) for the specified package full name.
old-location: appxpkg\packageidfromfullname.htm
old-project: appxpkg
ms.assetid: EED832F8-E4F7-4A0F-93E2-451F78F67767
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: PackageIdFromFullName, PackageIdFromFullName function [App packaging and management], appmodel/PackageIdFromFullName, appxpkg.packageidfromfullname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: appmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PackageOrigin
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-AppModel-Runtime-l1-1-0.dll
-	kernel32legacy.dll
-	Ext-MS-Win-kernel32-package-l1-1-0.dll
-	Kernel.AppCore.dll
-	API-MS-Win-AppModel-RunTime-l1-1-1.dll
-	Ext-MS-Win-Kernel32-package-l1-1-2.dll
-	ext-ms-win-kernel32-package-l1-1-1.dll
-	API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
-	PackageIdFromFullName
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# PackageIdFromFullName function


## -description


Gets the package identifier (ID) for the specified package full name.


## -parameters




### -param packageFullName [in]

Type: <b>PCWSTR</b>

The full name of a package.


### -param flags [in]

Type: <b>const UINT32</b>

The <a href="https://msdn.microsoft.com/72E565C3-6CFD-47E3-8BAC-17D6E86B99DA">package constants</a> that specify how package information is retrieved. The <b>PACKAGE_INFORMATION_*</b> flags are supported.


### -param bufferLength [in, out]

Type: <b>UINT32*</b>

On input, the size of <i>buffer</i>, in bytes. On output, the size of the data returned, in bytes.


### -param buffer [out, optional]

Type: <b>BYTE*</b>

The package ID, represented as a <a href="https://msdn.microsoft.com/4B15281A-2227-47B7-A750-0A01DB8543FC">PACKAGE_ID</a> structure.


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
The buffer is not large enough to hold the data. The required size is specified  by <i>bufferLength</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The package is not installed for the user.

</td>
</tr>
</table>
 




## -remarks



If <i>flags</i> specifies <b>PACKAGE_INFORMATION_BASIC</b>, the following fields are retrieved:

<ul>
<li><b>name</b></li>
<li><b>processorArchitecture</b></li>
<li><b>publisherId</b></li>
<li><b>resourceId</b></li>
<li><b>version</b></li>
</ul>
If <i>flags</i> specifies <b>PACKAGE_INFORMATION_FULL</b>, the following fields are retrieved:

<ul>
<li><b>name</b></li>
<li><b>processorArchitecture</b></li>
<li><b>publisher</b></li>
<li><b>publisherId</b></li>
<li><b>resourceId</b></li>
<li><b>version</b></li>
</ul>
A request for <b>PACKAGE_INFORMATION_FULL</b> succeeds only if the package corresponding to <i>packageFullName</i> is installed for and accessible to the current user. If the package full name is syntactically correct but does not correspond to a package that is installed for and accessible to the current user, the function returns <b>ERROR_NOT_FOUND</b>.

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
void FullNameToId(__in PCWSTR fullName, __in const UINT32 flags);
void ShowPackageId(__in const PACKAGE_ID * packageId);

int ShowUsage()
{
    wprintf(L"Usage: PackageIdFromFullName &lt;[flags]fullname&gt; [&lt;[flags]fullname&gt;...]\n"
            L"flags:\n"
            L"    ? = Basic information (PACKAGE_INFORMATION_BASIC)\n"
            L"    * = Full information (PACKAGE_INFORMATION_FULL)\n"
            L"Default = Basic\n");
    return 1;
}

int __cdecl wmain(__in int argc, __in_ecount(argc) WCHAR * argv[])
{
    if (argc &lt;= 1)
        return ShowUsage();

    for (int i=1; i&lt;argc; ++i)
    {
        PCWSTR fullName = argv[i];
        UINT32 flags = PACKAGE_INFORMATION_BASIC;
        if (*fullName != L'\0')
        {
            if (*fullName == L'?')
            {
                flags = PACKAGE_INFORMATION_BASIC;
                ++fullName;
            }
            else if (*fullName == L'*')
            {
                flags = PACKAGE_INFORMATION_FULL;
                ++fullName;
            }
        }
        FullNameToId(fullName, flags);
    }

    return 0;
}

void FullNameToId(__in PCWSTR fullName, __in const UINT32 flags)
{
    wprintf(L"FullName: %s%s\n", fullName, ((flags &amp; PACKAGE_INFORMATION_FULL) == 0 ? L"  [BASIC]" : L"  [FULL]"));
    UINT32 length = 0;
    LONG rc = PackageIdFromFullName(fullName, flags, &amp;length, NULL);
    if (rc == ERROR_SUCCESS)
    {
        wprintf(L"PackageIdFromFullName unexpected succeeded\n");
        return;
    }
    else if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        wprintf(L"Error %d in PackageIdFromFullName\n", rc);
        return;
    }

    BYTE * buffer = (PBYTE) malloc(length);
    if (buffer == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return;
    }

    rc = PackageIdFromFullName(fullName, flags, &amp;length, buffer);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d converting Package Full Name to Id\n", rc);
    else
    {
        ShowPackageId((PACKAGE_ID *) buffer);
    }

    free(buffer);
}

void ShowPackageId(__in const PACKAGE_ID * packageId)
{
    wprintf(L"    Name        : %s\n", packageId-&gt;name);
    if (packageId-&gt;publisher != NULL)
        wprintf(L"    Publisher   : %s\n", packageId-&gt;publisher);
    if (packageId-&gt;publisherId != NULL)
        wprintf(L"    PublisherId : %s\n", packageId-&gt;publisherId);
    wprintf(L"    Version     : %hu.%hu.%hu.%hu\n",
            packageId-&gt;version.Major,
            packageId-&gt;version.Minor,
            packageId-&gt;version.Build,
            packageId-&gt;version.Revision);
    wprintf(L"    Architecture: %u\n", packageId-&gt;processorArchitecture);
    if (packageId-&gt;resourceId != NULL)
        wprintf(L"    Resource    : %s\n", packageId-&gt;resourceId);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4CFC707A-2A5A-41FE-BB5F-6FECACC99271">GetCurrentPackageId</a>



<a href="https://msdn.microsoft.com/BA5D87F5-72FD-48BE-A104-EC7D1459FD58">GetPackageId</a>



<a href="https://msdn.microsoft.com/98E95CE5-E970-4A19-BAD3-994DAEC4BEA0">PackageFamilyNameFromFullName</a>



<a href="https://msdn.microsoft.com/198DAB6B-21D2-4ACB-87DF-B3F4EFBEE323">PackageFamilyNameFromId</a>



<a href="https://msdn.microsoft.com/0024AF55-295E-49B1-90C2-9144D336529B">PackageFullNameFromId</a>



<a href="https://msdn.microsoft.com/4AA5BD75-F865-40D6-9C10-E54C197D47C4">PackageNameAndPublisherIdFromFamilyName</a>
 

 

