---
UID: NF:rometadataresolution.RoParseTypeName
title: RoParseTypeName function
author: windows-sdk-content
description: Parses a type name and existing type parameters, in the case of parameterized types.
old-location: winrt\roparsetypename.htm
old-project: WinRT
ms.assetid: AF007D43-7BAC-4753-9D2B-8F397B4A464A
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: RoParseTypeName, RoParseTypeName function [Windows Runtime], rometadataresolution/RoParseTypeName, winrt.roparsetypename
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rometadataresolution.h
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
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WinTypes.dll
 - API-MS-Win-ro-typeresolution-l1-1-0.dll
 - Ext-MS-Win-Ro-TypeResolution-L1-1-0.dll
api_name:
 - RoParseTypeName
product: Windows
targetos: Windows
req.lib: WinTypes.lib
req.dll: WinTypes.dll
req.irql: 
req.product: ADAM
---

# RoParseTypeName function


## -description


Parses a type name and existing type parameters, in the case of parameterized types.


## -parameters




### -param typeName

TBD


### -param partsCount [out]

Type: <b>DWORD*</b>

Number of elements in the <i>typenameParts</i> array.


### -param typeNameParts

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>**</b>

The first element of the array is the specified type, and the remaining array elements are the type parameters (if any) in prewalk tree order.


#### - typename [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

String-encoded typename. The typename can be a non-namespace-qualified type, a non-parameterized namespace-qualified type or a fully instantiated namespace-qualified parameterized type.


## -returns



Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Parsing was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>typeName</i> contains embedded nulls or is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RO_E_METADATA_INVALID_TYPE_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
<i>typename</i> is not well formed.

</td>
</tr>
</table>
 




## -remarks



The <b>RoParseTypeName</b> function parses the string-encoded  type name and returns an array of <b>HSTRING</b> values. The first element of the array is the base type, and the remaining array elements are the type parameters, if any, in pre-order tree traversal order. <b>S_OK</b> is returned if the parsing was successful. 

Here are examples of different possible input typenames:

<ul>
<li>
Example 1 (non-namespace-qualified type)

<ul>
<li>
<b>Input typename</b>

String

</li>
<li>
<b>Output</b>

Array element 0: String

</li>
</ul>
</li>
<li>
Example 2 (non-parameterized namespace-qualified type)

<ul>
<li>
<b>Input typename</b>

Windows.Foundation.IExtensionInformation

</li>
<li>
<b>Output</b>

Array element 0: Windows.Foundation.IExtensionInformation

</li>
</ul>
</li>
<li>
Example 3 (instantiated parameterized interface type)

<ul>
<li>
<b>Input typename</b>

Windows.Foundation.Collections.IIterator`1&lt;Windows.Foundation.Collections.IMapView`2&lt;Windows.Foundation.Collections.IVector`1&lt;String&gt;, String&gt;&gt;

</li>
<li>
<b>Output</b>

Array element 0: Windows.Foundation.Collections.IIterator`1

Array element 1: Windows.Foundation.Collections.IMapView`2

Array element 2: Windows.Foundation.Collections.IVector`1

Array element 3: String

Array element 4: String

</li>
</ul>
</li>
</ul>
When parsing a non-parameterized type, the <b>RoParseTypeName</b> function returns an array that has one element. Please refer to example 1 and example 2 above.

The input string must be non-empty and it must not contain any embedded null characters. Otherwise, the API fails with <b>E_INVALIDARG</b>.  If the <i>typename</i> is ill-formed, like  IVector`1&lt;, then the API will fail with  the <b>RO_E_METADATA_INVALID_TYPE_FORMAT</b> error code.

The <b>RoParseTypeName</b> function validates only the format of the <i>typename</i> and not its syntax. For example, the function validates that a namespace-qualified parameterized interface <i>typename</i> follows the format shown in the following table, but it does not impose any requirements on what characters/symbols can be used in the <i>typename</i>, except that it should not contain ` , &lt;, or &gt; characters.

The format for a string-encoded instantiated parameterized interface is as follows:

<table>
<tr>
<td>
Name of parameterized interface

</td>
<td>
Backtick character
(`)

</td>
<td>
Number of type parameters

</td>
<td>
Left angle bracket (&lt;)

</td>
<td>
Namespace qualified name of each type parameter, separated by commas.

</td>
<td>
Right angle bracket
(&gt;)

</td>
</tr>
</table>
 

Type parameters may be:

<ul>
<li>Non-parameterized, non-namespace-qualified types, like  WinRT fundamental types.</li>
<li>Non-parameterized namespace-qualified types.</li>
<li>Fully-instantiated namespace-qualified parameterized interfaces.</li>
</ul>
On success, the caller is responsible for deallocating the <i>typenameParts</i> array returned by <b>RoParseTypeName</b> by using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to free the array and <a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a> to free the <b>HSTRING</b> values.


#### Examples

The following C++ example shows how to use the <b>RoParseTypeName</b> function to find the direct child namespaces for a specified type name.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;WinRTString.h&gt;
#include &lt;TypeResolution.h&gt;

HRESULT PrintParameterizedInterfaceParts(PCWSTR pszTypename);

int ShowUsage()
{
    wprintf(L"Usage: RoParseTypeNameSample \"TypeName\"\n");
    return -1;
}

int __cdecl wmain(int argc, WCHAR **argv)
{
    if (argc != 2)
    {
        return ShowUsage();
    }

    HRESULT hr = PrintParameterizedInterfaceParts(argv[1]);

    if (SUCCEEDED(hr))
    {
        return 0;
    }
    else
    {
        return -1;
    }
}

HRESULT PrintParameterizedInterfaceParts(PCWSTR pszTypename)
{
    HRESULT hr;
    HSTRING hstrTypeName = nullptr;
    HSTRING *phstrNameParts = nullptr;
    DWORD cRetrievedNameParts = 0;

    hr = WindowsCreateString(
        pszTypename,
        static_cast&lt;UINT32&gt;(wcslen(pszTypename)),
        &amp;hstrTypeName);

    if (SUCCEEDED(hr))
    {
        hr = RoParseTypeName(
            hstrTypeName,
            &amp;cRetrievedNameParts,
            &amp;phstrNameParts);
    }

    if (SUCCEEDED(hr))
    {
        wprintf(L"Parameterized interface %s is composed of:\n", pszTypename);

        for (UINT32 i = 0; i &lt; cRetrievedNameParts; i++)
        {
            wprintf(L"Element %d: %s\n", i, WindowsGetStringRawBuffer(phstrNameParts[i], nullptr));
        }
    }
    else
    {
        wprintf(L"Invalid parameterized interface syntax: %s!\n", pszTypename);
    }

    // Clean up resources.
    if (hstrTypeName != nullptr)
    {
        WindowsDeleteString(hstrTypeName);
    }

    for (UINT32 i = 0; i &lt; cRetrievedNameParts; i++)
    {
        WindowsDeleteString(phstrNameParts[i]);
    }

    CoTaskMemFree(phstrNameParts);

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


