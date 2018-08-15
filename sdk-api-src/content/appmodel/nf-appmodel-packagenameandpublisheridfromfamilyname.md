---
UID: NF:appmodel.PackageNameAndPublisherIdFromFamilyName
title: PackageNameAndPublisherIdFromFamilyName function
author: windows-sdk-content
description: Gets the package name and publisher identifier (ID) for the specified package family name.
old-location: appxpkg\packagenameandpublisheridfromfamilyname.htm
old-project: appxpkg
ms.assetid: 4AA5BD75-F865-40D6-9C10-E54C197D47C4
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: PackageNameAndPublisherIdFromFamilyName, PackageNameAndPublisherIdFromFamilyName function [App packaging and management], appmodel/PackageNameAndPublisherIdFromFamilyName, appxpkg.packagenameandpublisheridfromfamilyname
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
 - Kernel.AppCore.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - PackageNameAndPublisherIdFromFamilyName
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# PackageNameAndPublisherIdFromFamilyName function


## -description


Gets the package name and publisher identifier (ID) for the specified package family name.


## -parameters




### -param packageFamilyName [in]

Type: <b>PCWSTR</b>

The family name of a package.


### -param packageNameLength [in, out]

Type: <b>UINT32*</b>

On input, the size of the <i>packageName</i> buffer, in characters. On output, the size of the package name returned, in characters, including the null-terminator.


### -param packageName [out, optional]

Type: <b>PWSTR</b>

The package name.


### -param packagePublisherIdLength [in, out]

Type: <b>UINT32*</b>

On input, the size of the <i>packagePublishId</i> buffer, in characters. On output, the size of the publisher ID returned, in characters, including the null-terminator.


### -param packagePublisherId [out, optional]

Type: <b>PWSTR</b>

The package publisher ID.


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
One of the buffers is not large enough to hold the data. The required sizes are specified  by <i>packageNameLength</i> and <i>packagePublisherIdLength</i>.

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
void FamilyNameToNameAndPublisherId(__in PCWSTR familyName);

int ShowUsage()
{
    wprintf(L"Usage: PackageNameAndPublisherIdFromFamilyName &lt;familyname&gt; [&lt;familyname&gt;...]\n");
    return 1;
}

int __cdecl wmain(__in int argc, __in_ecount(argc) WCHAR * argv[])
{
    if (argc &lt;= 1)
        return ShowUsage();

    for (int i=1; i&lt;argc; ++i)
        FamilyNameToNameAndPublisherId(argv[i]);

    return 0;
}

void FamilyNameToNameAndPublisherId(__in PCWSTR familyName)
{
    wprintf(L"FamilyName: %s\n", familyName);
    UINT32 nameLength = 0;
    UINT32 publisherIdLength = 0;
    LONG rc = PackageNameAndPublisherIdFromFamilyName(familyName, &amp;nameLength, NULL, &amp;publisherIdLength, NULL);
    if (rc == ERROR_SUCCESS)
    {
        wprintf(L"PackageNameAndPublisherIdFromFamilyName unexpectedly succeeded\n");
        return;
    }
    else if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        wprintf(L"Error %d in PackageNameAndPublisherIdFromFamilyName\n", rc);
        return;
    }

    PWSTR name = (PWSTR) malloc(nameLength * sizeof(WCHAR));
    if (name == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return;
    }

    PWSTR publisherId = (PWSTR) malloc(publisherIdLength * sizeof(WCHAR));
    if (publisherId == NULL)
    {
        wprintf(L"Error allocating memory\n");
        free(name);
        return;
    }

    rc = PackageNameAndPublisherIdFromFamilyName(familyName, &amp;nameLength, name, &amp;publisherIdLength, publisherId);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d converting PackageFamilyName to Name and PublisherId\n", rc);
    else
    {
        wprintf(L"        Name = %s\n", name);
        wprintf(L"Publisher Id = %s\n", publisherId);
    }

    free(name);
    free(publisherId);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/98E95CE5-E970-4A19-BAD3-994DAEC4BEA0">PackageFamilyNameFromFullName</a>



<a href="https://msdn.microsoft.com/198DAB6B-21D2-4ACB-87DF-B3F4EFBEE323">PackageFamilyNameFromId</a>



<a href="https://msdn.microsoft.com/0024AF55-295E-49B1-90C2-9144D336529B">PackageFullNameFromId</a>



<a href="https://msdn.microsoft.com/EED832F8-E4F7-4A0F-93E2-451F78F67767">PackageIdFromFullName</a>
 

 

