---
UID: NF:rometadataresolution.RoGetMetaDataFile
title: RoGetMetaDataFile function (rometadataresolution.h)
description: Locates and retrieves the metadata file that describes the Application Binary Interface (ABI) for the specified typename.
helpviewer_keywords: ["RoGetMetaDataFile","RoGetMetaDataFile function [Windows Runtime]","rometadataresolution/RoGetMetaDataFile","winrt.rogetmetadatafile"]
old-location: winrt\rogetmetadatafile.htm
tech.root: WinRT
ms.assetid: FF4FEA9F-3FB0-4D56-BE9A-E8E2CB13D718
ms.date: 11/19/2021
ms.keywords: RoGetMetaDataFile, RoGetMetaDataFile function [Windows Runtime], rometadataresolution/RoGetMetaDataFile, winrt.rogetmetadatafile
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
req.lib: WindowsApp.lib
req.dll: WinTypes.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoGetMetaDataFile
 - rometadataresolution/RoGetMetaDataFile
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
 - RoGetMetaDataFile
---

# RoGetMetaDataFile function


## -description

Locates and retrieves the metadata file that describes the Application Binary Interface (ABI) for the specified typename.

## -parameters

### -param name [in]

Type: <b>const <a href="/windows/desktop/WinRT/hstring">HSTRING</a></b>

The name to resolve, either a typename or a namespace. The name input string must be non-empty and must not contain embedded NUL characters. If the name is a dot-separated string, then the substring to the left of the last dot and the substring to the right of the last dot must be non-empty.

### -param metaDataDispenser [in, optional]

Type: <b>IMetaDataDispenserEx*</b>

A metadata dispenser that the caller can optionally pass in for the <b>RoGetMetaDataFile</b> function to be able to open the metadata files through the provided <b>IMetaDataDispenserEx::OpenScope</b> method. If the metadata dispenser parameter is set to <b>nullptr</b>, the function creates an internal instance of the refactored metadata reader (RoMetadata.dll) and uses its <b>IMetaDataDispenserEx::OpenScope</b> method. You can create a metadata dispenser using the <a href="/windows/win32/api/rometadata/nf-rometadata-metadatagetdispenser">MetaDataGetDispenser</a> function.

### -param metaDataFilePath [out, optional]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a>*</b>

The absolute path of the metadata (.winmd) file that describes the ABI, unless set to <b>nullptr</b>. The caller is responsible for freeing the <a href="/windows/desktop/WinRT/hstring">HSTRING</a> by calling the <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a> method.

### -param metaDataImport [out, optional]

Type: <b>IMetaDataImport2**</b>

A pointer to the metadata file reader object. If the caller passes in a <b>nullptr</b> ,  the function releases the <b>IMetaDataImport2</b> reference, otherwise the caller must release the reference. The value is set to <b>nullptr</b> on failure.

### -param typeDefToken [out, optional]

Type: <b>mdTypeDef*</b>

If the name input string is resolved successfully as a typename, this parameter is set to the  token of the typename.

On failure, this parameter is set to <b>mdTypeDefNil</b>.

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
Resolution was successful, which means that the input string represents a type defined in a .winmd file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following properties of the input name string does not hold:

<ul>
<li>Not null, not empty</li>
<li>Does not contain embedded null characters.</li>
<li>If a dot-separated string, the substring to the left of the last dot and the substring to the right of the last dot must be non-empty.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RO_E_METADATA_NAME_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The input string is not a type defined in any examined .winmd file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RO_E_METADATA_NAME_IS_NAMESPACE</b></dt>
</dl>
</td>
<td width="60%">
The input string is an existing namespace rather than a typename.

</td>
</tr>
</table>

## -remarks

The caller can optionally pass-in a metadata dispenser for the <b>RoGetMetaDataFile</b> function to open the metadata files through the <b>IMetaDataDispenserEx::OpenScope</b> method. 

If the metadata dispenser parameter is set to <b>nullptr</b>, the function creates an internal instance of the refactored metadata reader and uses that reader’s <b>IMetaDataDispenserEx::OpenScope</b> method.



The <b>RoGetMetaDataFile</b> function is guaranteed to be thread-safe if you pass-in <b>nullptr</b> to the metadata dispenser parameter, as the function creates an internal read-only metadata reader. This guarantee also holds if you pass in the read-only metadata reader, like  RoMetadata to the function.



All three output parameters are optional and none of them needs to be specified. Calling the <b>RoGetMetaDataFile</b> function with <b>nullptr</b> for all output parameters is equivalent to asking whether the input typename or namespace is defined.



The metadata reader object reference and the TypeDef token parameters paired, so both must be set together or be set to  <b>nullptr</b>.  


There are three possible type resolution scenarios:

<table>
<tr>
<td>
Scenario #1

</td>
<td>
<b>Typename input string is a type defined in a WinMD file.</b>

<ul>
<li>
Return Value

<b>S_OK</b>

</li>
<li>
Metadata file path output parameter

This is an optional output parameter. If not set to <b>nullptr</b> by caller, it holds the absolute path of the .winmd file that describes the given type's ABI. The caller is responsible for freeing the <b>HSTRING</b> by calling <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>.

</li>
<li>
Reference to the metadata reader object output parameter

This is an optional output parameter. If not <b>nullptr</b>, it holds a reference to the metadata reader object (<b>IMetaDataImport2</b>) and the caller is responsible for releasing it. If the caller passes <b>nullptr</b> for this parameter, it means that the caller does not want the metadata reader object, so the function releases the internal reference.

</li>
<li>
Typedef token output parameter

This is an optional output parameter. If not set to <b>nullptr</b> by caller, it is set to the token of the type’s <b>typedef</b> entry. Language projections can use this token to call <b>IMetaDataImport::GetTypeDefProps</b> to get metadata about the type.

</li>
</ul>
</td>
</tr>
<tr>
<td>
Scenario #2

</td>
<td><b>Typename input string is actually an existing namespace rather than a typename.</b><ul>
<li>
Return value

<b>RO_E_METADATA_NAME_IS_NAMESPACE</b>

</li>
<li>
Metadata file path output parameter

This is an optional output parameter. If not set to <b>nullptr</b> by the caller, it is set to <b>nullptr</b>.

</li>
<li>
Reference to the metadata reader object output parameter

This is an optional output parameter. If not set to <b>nullptr</b> by caller, it is set to <b>nullptr</b>.

</li>
<li>
Typedef token output parameter

This is an optional output parameter. If not set to <b>nullptr</b> by caller, it will is to <b>mdTypeDefNil</b>.

</li>
</ul>
</td>
</tr>
<tr>
<td>
Scenario #3

</td>
<td><b>Input string is not a type defined in any examined WinMD file</b><ul>
<li>
Return value

<b>RO_E_METADATA_NAME_NOT_FOUND</b>

</li>
<li>
Metadata file path output parameter

This is an optional output parameter. If not set to <b>nullptr</b> by caller, it is set to <b>nullptr</b>

</li>
<li>
Reference to the metadata reader object output parameter

This is an optional output parameter. If not set to <b>nullptr</b> by caller, it is set to <b>nullptr</b>

</li>
<li>
Typedef token output parameter

This is an optional output parameter. If not set to <b>nullptr</b> by caller, it is set to <b>mdTypeDefNil</b>.

</li>
</ul>
</td>
</tr>
</table>
 

The <b>RoGetMetaDataFile</b> function resolves an <b>interfacegroup</b>, because the <b>interfacegroup</b> also is a namespace-qualified typename. The <a href="/windows/desktop/api/inspectable/nf-inspectable-iinspectable-getruntimeclassname">IInspectable::GetRuntimeClassName</a> method returns the string in dot-separated string format for use by <b>RoGetMetaDataFile</b>.

Resolving 3rd-party types from a process that's not in a Windows Store app is not supported. In this case, the function returns error <b>HRESULT_FROM_WIN32(ERROR_NO_PACKAGE)</b> and sets output parameters to <b>nullptr</b>. But Windows types are resolved in a process that's not in a Windows Store app.


#### Examples

The following C++ example shows how to use the <b>RoGetMetaDataFile</b> function to find the metadata file for a specified type name.


```cpp
#include <windows.h>
#include <stdio.h>
#include <WinRTString.h>
#include <TypeResolution.h>
#include <atlbase.h>

HRESULT PrintMetaDataFilePathForTypeName(PCWSTR pszTypename);

int ShowUsage()
{
    wprintf(L"Usage: RoGetMetaDataFileSample TypeName\n");
    return -1;
}

int __cdecl wmain(int argc, WCHAR **argv)
{
    if (argc != 2)
    {
        return ShowUsage();
    }

    HRESULT hr = PrintMetaDataFilePathForTypeName(argv[1]);

    if (SUCCEEDED(hr))
    {
        return 0;
    }
    else
    {
        return -1;
    }
}

HRESULT PrintMetaDataFilePathForTypeName(PCWSTR pszTypename)
{
    HRESULT hr;
    HSTRING hstrTypeName = nullptr;
    HSTRING hstrMetaDataFilePath = nullptr;
    CComPtr<IMetaDataImport2> spMetaDataImport;
    mdTypeDef typeDef;

    hr = WindowsCreateString(
        pszTypename,
        static_cast<UINT32>(wcslen(pszTypename)),
        &hstrTypeName);

    if (SUCCEEDED(hr))
    {
        hr = RoGetMetaDataFile(
            hstrTypeName,
            nullptr,
            &hstrMetaDataFilePath,
            &spMetaDataImport,
            &typeDef);
    }

    if (SUCCEEDED(hr))
    {
        wprintf(L"Type %s was found in %s\n", pszTypename,  WindowsGetStringRawBuffer(hstrMetaDataFilePath, nullptr));
    }
    else if (hr == RO_E_METADATA_NAME_NOT_FOUND)
    {
        wprintf(L"Type %s was not found!\n", pszTypename);
    }
    else
    {
        wprintf(L"Error %x occurred while trying to resolve %s!\n", hr, pszTypename);
    }

    // Clean up resources.
    if (hstrTypeName != nullptr)
    {
        WindowsDeleteString(hstrTypeName);
    }

    if (hstrMetaDataFilePath != nullptr)
    {
        WindowsDeleteString(hstrMetaDataFilePath);
    }

    return hr;
}

```
