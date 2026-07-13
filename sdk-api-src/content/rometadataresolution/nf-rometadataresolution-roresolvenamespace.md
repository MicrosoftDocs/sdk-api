---
UID: NF:rometadataresolution.RoResolveNamespace
title: RoResolveNamespace function (rometadataresolution.h)
description: Determine the direct children, types, and sub-namespaces of the specified Windows Runtime namespace, from any programming language supported by the Windows Runtime.
helpviewer_keywords: ["RoResolveNamespace","RoResolveNamespace function [Windows Runtime]","rometadataresolution/RoResolveNamespace","winrt.roresolvenamespace"]
old-location: winrt\roresolvenamespace.htm
tech.root: WinRT
ms.assetid: 597E8B18-B9D9-42E5-B260-595370BEEAC0
ms.date: 12/05/2018
ms.keywords: RoResolveNamespace, RoResolveNamespace function [Windows Runtime], rometadataresolution/RoResolveNamespace, winrt.roresolvenamespace
req.header: rometadataresolution.h
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
req.lib: WinTypes.lib
req.dll: WinTypes.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoResolveNamespace
 - rometadataresolution/RoResolveNamespace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ro-typeresolution-l1-1-1.dll
 - api-ms-win-ro-typeresolution-l1-1-1.dll
 - WinTypes.dll
 - API-MS-Win-ro-typeresolution-l1-1-0.dll
 - Ext-MS-Win-Ro-TypeResolution-L1-1-0.dll
api_name:
 - RoResolveNamespace
---

# RoResolveNamespace function


## -description

Determine the direct children, types, and sub-namespaces of the specified Windows Runtime namespace, from any programming language supported by the Windows Runtime.

## -parameters

### -param name [in, optional]

Type: <b>const <a href="/windows/desktop/WinRT/hstring">HSTRING</a></b>

Full namespace for which we are trying to retrieve direct children. This is a required parameter.

If this namespace is empty or <b>nullptr</b>, the <b>RoResolveNamespace</b> function returns top-level namespaces. Both Windows  and other top-level namespaces are in the package graph.

### -param windowsMetaDataDir [in, optional]

Type: <b>const <a href="/windows/desktop/WinRT/hstring">HSTRING</a></b>

Optional parameter that contains a path to the SDK directory to search for metadata (.winmd) files.

If this parameter is not specified (either empty or <b>nullptr</b>), the function searches in the default Windows metadata directory, %windir%\System32\WinMetadata.

### -param packageGraphDirsCount [in]

Type: <b>const DWORD</b>

Count of paths in the <i>packageGraphDirs</i> array.

### -param packageGraphDirs [in, optional]

Type: <b>const <a href="/windows/desktop/WinRT/hstring">HSTRING</a>*</b>

Count of package paths in the explicit package dependency graph array. The count is ignored if <i>packageGraphDirs</i> is <b>nullptr</b>.

### -param metaDataFilePathsCount [out, optional]

Type: <b>DWORD*</b>

Count of metadata files in the <i>metaDataFilePaths</i> array.

### -param metaDataFilePaths [out, optional]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a>**</b>

Optional output parameter that contains callee-allocated array of absolute file paths of all metadata (.winmd) files that could possibly contain direct children of <i>name</i>.

### -param subNamespacesCount [out, optional]

Type: <b>DWORD*</b>

Count of metadata files in the <i>subNamespaces</i> array.

### -param subNamespaces [out, optional]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a>**</b>

Optional output parameter that contains a callee-allocated array of names of direct children of the given namespace. This list is a hint of other subnamespaces and is not necessarily complete.

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
Namespace direct children resolution is successful, which means that at least one file or one subnamespace name was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RO_E_METADATA_NAME_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates one of the following:

<ul>
<li><i>metaDataFilePaths</i> and <i>subNamespaces</i> output parameters are set, but no metadata files and no subnamespaces for the given namespace were found.</li>
<li><i>metaDataFilePaths</i> only is set, but no metadata files for the given namespace were found.</li>
<li><i>subNamespaces</i> only is set, but no subnamespaces for the given namespace were found.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates one of the following:

<ul>
<li>Both <i>metaDataFilePaths</i> and <i>subNamespaces</i> are not set.</li>
<li>Namespace name has embedded null characters.</li>
<li>Namespace is empty or <b>NULL</b> and <i>subNamespaces</i> is not set.</li>
<li>Namespace is empty or <b>NULL</b> and <i>metaDataFilePaths</i> is set.</li>
</ul>
</td>
</tr>
</table>

## -remarks

Use the <b>RoResolveNamespace</b> function to explore Windows Runtime namespace hierarchies.


#### Examples

The following C++ example shows how to use the <b>RoResolveNamespace</b> function to find the direct child namespaces for a specified type name.


```cpp
#include <windows.h>
#include <stdio.h>
#include <WinRTString.h>
#include <TypeResolution.h>
#include <atlbase.h>

HRESULT PrintDirectChildrenSubNamespacesAndTypesPaths(PCWSTR pszName);

int ShowUsage()
{
    wprintf(L"Usage: RoResolveNamespaceSample TypeName\n");
    return -1;
}

int __cdecl wmain(int argc, WCHAR **argv)
{
    if (argc != 2)
    {
        return ShowUsage();
    }

    HRESULT hr = PrintDirectChildrenSubNamespacesAndTypesPaths(argv[1]);

    if (SUCCEEDED(hr))
    {
        return 0;
    }
    else
    {
        return -1;
    }
}

HRESULT PrintDirectChildrenSubNamespacesAndTypesPaths(PCWSTR pszName)
{
    HRESULT hr;
    HSTRING hstrName = nullptr;
    DWORD cRetrievedSubNamespaces = 0;
    HSTRING *phstrRetrievedSubNamespaces = nullptr;
    DWORD cRetrievedMetaDataFilePaths = 0;
    HSTRING *phstrRetrievedMetaDataFiles = nullptr;

    hr = WindowsCreateString(
        pszName,
        static_cast<UINT32>(wcslen(pszName)),
        &hstrName);

    if (SUCCEEDED(hr))
    {
        hr = RoResolveNamespace(
            hstrName,
            nullptr,
            0,
            nullptr,
            &cRetrievedMetaDataFilePaths,
            &phstrRetrievedMetaDataFiles,
            &cRetrievedSubNamespaces,
            &phstrRetrievedSubNamespaces);
    }

    if (SUCCEEDED(hr))
    {
        if (cRetrievedSubNamespaces != 0)
        {
            wprintf(L"Direct-children subnamespaces of %s are:\n", pszName);

            for (DWORD i = 0; i < cRetrievedSubNamespaces; i++)
            {
                wprintf(L"Subnamespace %d: %s\n", i, WindowsGetStringRawBuffer(phstrRetrievedSubNamespaces[i], nullptr));
            }
        }

        if (cRetrievedMetaDataFilePaths != 0)
        {
            wprintf(L"Potential direct-children types of %s could be found in:\n", pszName);

            for (DWORD i = 0; i < cRetrievedMetaDataFilePaths; i++)
            {
                wprintf(L"Metadata file path %d: %s\n", i, WindowsGetStringRawBuffer(phstrRetrievedMetaDataFiles[i], nullptr));
            }
        }
    }
    else if (hr == RO_E_METADATA_NAME_NOT_FOUND)
    {
        wprintf(L"Name %s was not found!\n", pszName);
    }
    else
    {
        wprintf(L"Error %x occurred while trying to resolve %s!\n", hr, pszName);
    }

    // Clean up resources.
    if (hstrName != nullptr)
    {
        WindowsDeleteString(hstrName);
    }

    for (DWORD i = 0; i < cRetrievedSubNamespaces; i++)
    {
        WindowsDeleteString(phstrRetrievedSubNamespaces[i]);
    }

    CoTaskMemFree(phstrRetrievedSubNamespaces);

    for (DWORD i = 0; i < cRetrievedMetaDataFilePaths; i++)
    {
        WindowsDeleteString(phstrRetrievedMetaDataFiles[i]);
    }
    
    CoTaskMemFree(phstrRetrievedMetaDataFiles);

    return hr;
}

```