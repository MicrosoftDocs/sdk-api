---
UID: NF:winnls.GetFileMUIInfo
title: GetFileMUIInfo function (winnls.h)
description: Retrieves resource-related information about a file.
helpviewer_keywords: ["GetFileMUIInfo","GetFileMUIInfo function [Internationalization for Windows Applications]","MUI_QUERY_CHECKSUM","MUI_QUERY_LANGUAGE_NAME","MUI_QUERY_RESOURCE_TYPES","MUI_QUERY_TYPE","_win32_GetFileMUIInfo","intl.getfilemuiinfo","winnls/GetFileMUIInfo"]
old-location: intl\getfilemuiinfo.htm
tech.root: Intl
ms.assetid: df1eee13-012a-47e6-a6de-8ddb8ecc6036
ms.date: 12/05/2018
ms.keywords: GetFileMUIInfo, GetFileMUIInfo function [Internationalization for Windows Applications], MUI_QUERY_CHECKSUM, MUI_QUERY_LANGUAGE_NAME, MUI_QUERY_RESOURCE_TYPES, MUI_QUERY_TYPE, _win32_GetFileMUIInfo, intl.getfilemuiinfo, winnls/GetFileMUIInfo
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetFileMUIInfo
 - winnls/GetFileMUIInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - GetFileMUIInfo
---

# GetFileMUIInfo function


## -description

Retrieves resource-related information about a file.

## -parameters

### -param dwFlags [in]

Flags specifying the information to retrieve. Any combination of the following flags is allowed. The default value of the flags is MUI_QUERY_TYPE | MUI_QUERY_CHECKSUM.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_QUERY_TYPE"></a><a id="mui_query_type"></a><dl>
<dt><b>MUI_QUERY_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve one of the following values in the <b>dwFileType</b> member of <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a>:

<ul>
<li>MUI_FILETYPE_NOT_LANGUAGE_NEUTRAL: The specified input file does not have resource configuration data. Thus it is neither an LN file nor a language-specific resource file. This type of file is typical for older executable files. If this file type is specified, the function will not retrieve useful information for the other types.</li>
<li>MUI_FILETYPE_LANGUAGE_NEUTRAL_MAIN. The input file is an LN file.</li>
<li>MUI_FILETYPE_LANGUAGE_NEUTRAL_MUI. The input file is a language-specific resource file associated with an LN file.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="MUI_QUERY_CHECKSUM"></a><a id="mui_query_checksum"></a><dl>
<dt><b>MUI_QUERY_CHECKSUM</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the resource checksum of the input file in the <b>pChecksum</b> member of <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a>. If the input file does not have resource configuration data, this member of the structure contains 0.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_QUERY_LANGUAGE_NAME"></a><a id="mui_query_language_name"></a><dl>
<dt><b>MUI_QUERY_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the language associated with the input file. For a language-specific resource file, this flag requests the associated language. For an LN file, this flag requests the language of the ultimate fallback resources for the module, which can be either in the LN file or in a separate language-specific resource file referenced by the resource configuration data of the LN file. For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_QUERY_RESOURCE_TYPES"></a><a id="mui_query_resource_types"></a><dl>
<dt><b>MUI_QUERY_RESOURCE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
Retrieve lists of resource types in the language-specific resource files and LN files as they are specified in the resource configuration data. See the Remarks section for a way to access this information.

</td>
</tr>
</table>

### -param pcwszFilePath [in]

Pointer to a null-terminated string indicating the path to the file. Typically the file is either an LN file or a language-specific resource file. If it is not one of these types, the only significant value that the function retrieves is MUI_FILETYPE_NOT_LANGUAGE_NEUTRAL. The function only retrieves this value if the MUI_QUERY_RESOURCE_TYPES flag is set.

### -param pFileMUIInfo [in, out, optional]

Pointer to a buffer containing file information in a <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure and possibly in data following that structure. The information buffer might have to be much larger than the size of the structure itself. Depending on flag settings, the function can store considerable information following the structure, at offsets retrieved in the structure. For more information, see the Remarks section.

Alternatively, the application can set this parameter to <b>NULL</b> if <i>pcbFileMUIInfo</i> is set to 0. In this case, the function retrieves the required size for the information buffer in <i>pcbFileMUIInfo</i>.

<div class="alert"><b>Note</b>  If the value of <i>pFileMUIInfo</i> is not <b>NULL</b>, the <b>dwSize</b> member must be set to the size of the <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure (including the information buffer), and the <b>dwVersion</b> member must be set to the current version of 0x001.</div>
<div> </div>

### -param pcbFileMUIInfo [in, out]

Pointer to the buffer size, in bytes, for the file information indicated by <i>pFileMUIInfo</i>. On successful return from the function, this parameter contains the size of the retrieved file information buffer and the <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure that contains it.

Alternatively, the application can set this parameter to 0 if it sets <b>NULL</b> in <i>pFileMUIInfo</i>. In this case, the function retrieves the required file information buffer size in <i>pcbFileMUIInfo</i>. To allocate the correct amount of memory, this value should be added to the size of the <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure itself.

<div class="alert"><b>Note</b>  The value of this parameter must match the value of the <b>dwSize</b> member of <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> if the value of <i>pFileMUIInfo</i> is not <b>NULL</b>.</div>
<div> </div>

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For the MUI_QUERY_LANGUAGE_NAME flag, this function retrieves an offset, in bytes, from the beginning of <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> in the <b>dwLanguageNameOffset</b> member.

The following is sample code that accesses the language name associated with the input file:


```cpp
LPWSTR lpszLang = reinterpret_cast<LPWSTR>(
        reinterpret_cast<BYTE*>(pFileMUIInfo) +
        pFileMUIInfo->dwLanguageNameOffset);

```


For the MUI_QUERY_RESOURCE_TYPES flag, this function retrieves language-specific resource file information in the following <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> members:

<ul>
<li>The <b>dwTypeIDMUIOffset</b> member contains the offset to an array of identifiers of resources contained in the language-specific resource file.</li>
<li>The <b>dwTypeIDMUISize</b> member contains the size of the array of resource identifiers for the language-specific resource file.</li>
<li>The <b>dwTypeNameMUIOffset</b> member contains the offset to an array of names of resources contained in the language-specific resource file.</li>
</ul>
If the input file is an LN file, the function fills in all the above structure members. In addition, it fills in the following members:

<ul>
<li>The <b>dwTypeIDMainOffset</b> member contains the offset to an array of identifiers of resources contained in the LN file.</li>
<li>The <b>dwTypeIDMainSize</b> member contains the size of the array of resource identifiers for the LN file.</li>
<li>The <b>dwTypeNameMainOffset</b> member contains the offset to an array of names of resources contained in the file.</li>
</ul>
The following is sample code that accesses the array of resource identifiers in the LN file.


```cpp
DWORD *pdwTypeID = reinterpret_cast<DWORD *>(
        reinterpret_cast<BYTE*>(pFileMUIInfo) +
        pFileMUIInfo->dwTypeIDMainOffset);

```


<div class="alert"><b>Note</b>  The lists of language-specific resources are accessed in the same way.</div>
<div> </div>
The following is sample code to access the multistring array of resource names in the LN file.


```cpp
LPWSTR lpszNames = reinterpret_cast<LPWSTR>(
        reinterpret_cast<BYTE*>(pFileMUIInfo) +
        pFileMUIInfo->dwTypeNameMainOffset);

```


<div class="alert"><b>Note</b>  The lists of language-specific resources are accessed in the same way.</div>
<div> </div>
Each of the code samples uses two reinterpret casts. First the code casts to BYTE* so that the pointer arithmetic for the offset is done in bytes. Then the code casts the resulting pointer to the desired type.

Another approach is to write the following instead of the code shown in the samples. The effect is the same and the choice is strictly one of style.


```cpp
DWORD ix = pFileMUIInfo->dwLanguageNameOffset - 
        offsetof(struct _FILEMUIINFO, abBuffer);
LPWSTR lpszLang = reinterpret_cast<LPWSTR>(&(pFileMUIInfo->abBuffer[ix]));

```


<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean GetFileMUIInfo(
            System.UInt32 dwFlags,
            System.String pcwszFilePath,
            ref FILEMUIINFO pFileMUIInfo,
            ref System.UInt32 pcbFileMUIInfo
            );

```

## -see-also

<a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getthreaduilanguage">GetThreadUILanguage</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setthreadpreferreduilanguages">SetThreadPreferredUILanguages</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setthreaduilanguage">SetThreadUILanguage</a>