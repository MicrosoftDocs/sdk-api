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
 

 

