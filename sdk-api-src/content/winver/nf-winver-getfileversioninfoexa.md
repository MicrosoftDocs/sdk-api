---
UID: NF:winver.GetFileVersionInfoExA
title: GetFileVersionInfoExA function (winver.h)
description: Retrieves version information for the specified file. (GetFileVersionInfoExA)
helpviewer_keywords: ["FILE_VER_GET_LOCALISED", "FILE_VER_GET_NEUTRAL", "FILE_VER_GET_PREFETCHED", "GetFileVersionInfoExA", "winver/GetFileVersionInfoExA"]
old-location: menurc\getfileversioninfoex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\versioninformation\versioninformationreference\versioninformationfunctions\getfileversioninfoex.htm
ms.date: 12/05/2018
ms.keywords: FILE_VER_GET_LOCALISED, FILE_VER_GET_NEUTRAL, FILE_VER_GET_PREFETCHED, GetFileVersionInfoEx, GetFileVersionInfoEx function [Menus and Other Resources], GetFileVersionInfoExA, GetFileVersionInfoExW, _win32_GetFileVersionInfoEx, _win32_getfileversioninfoex_cpp, menurc.getfileversioninfoex, winui._win32_getfileversioninfoex, winver/GetFileVersionInfoEx, winver/GetFileVersionInfoExA, winver/GetFileVersionInfoExW
req.header: winver.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFileVersionInfoExW (Unicode) and GetFileVersionInfoExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Version.lib
req.dll: Api-ms-win-core-version-l1-1-0.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetFileVersionInfoExA
 - winver/GetFileVersionInfoExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-version-l1-1-0.dll
 - API-MS-Win-Core-version-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-versionansi-l1-1-0.dll
 - API-MS-Win-DownLevel-version-l1-1-0.dll
 - API-MS-Win-Core-Versionansi-L1-1-1.dll
 - API-MS-Win-Core-Version-L1-1-1.dll
 - version.dll
api_name:
 - GetFileVersionInfoEx
 - GetFileVersionInfoExA
 - GetFileVersionInfoExW
---

# GetFileVersionInfoExA function


## -description

Retrieves version information for the specified file.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

Controls the MUI DLLs (if any) from which the version resource is extracted. The value of this flag must match the flags passed to the corresponding <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfosizeexa">GetFileVersionInfoSizeEx</a> call, which was used to determine the buffer size that is passed in the <i>dwLen</i> parameter. Zero or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_VER_GET_LOCALISED"></a><a id="file_ver_get_localised"></a><dl>
<dt><b>FILE_VER_GET_LOCALISED</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Loads the entire version resource (both strings and binary version information) from the corresponding MUI file, if available.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_VER_GET_NEUTRAL"></a><a id="file_ver_get_neutral"></a><dl>
<dt><b>FILE_VER_GET_NEUTRAL</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Loads the version resource strings from the corresponding MUI file, if available, and loads the binary version information (<b>VS_FIXEDFILEINFO</b>) from the corresponding language-neutral file, if available. 

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_VER_GET_PREFETCHED"></a><a id="file_ver_get_prefetched"></a><dl>
<dt><b>FILE_VER_GET_PREFETCHED</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Indicates a preference for version.dll to attempt to preload the image outside of the loader lock to avoid contention.  This flag does not change the behavior or semantics of the function.

</td>
</tr>
</table>

### -param lpwstrFilename [in]

Type: <b>LPCTSTR</b>

The name of the file. If a full path is not specified, the function uses the search sequence specified by the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function.

### -param dwHandle

Type: <b>DWORD</b>

This parameter is reserved, and expected to be zero (0).

### -param dwLen [in]

Type: <b>DWORD</b>

The size, in bytes, of the buffer pointed to by the <i>lpData</i> parameter. 

                    

Call the <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfosizeexa">GetFileVersionInfoSizeEx</a> function first to determine the size, in bytes, of a file's version information. The <i>dwLen</i> parameter should be equal to or greater than that value.

If the buffer pointed to by <i>lpData</i> is not large enough, the function truncates the file's version information to the size of the buffer.

### -param lpData [out]

Type: <b>LPVOID</b>

When this function returns, contains a pointer to a buffer that contains the file-version information.

You can use this value in a subsequent call to the <a href="/windows/desktop/api/winver/nf-winver-verqueryvaluea">VerQueryValue</a> function to retrieve data from the buffer.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Call the <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfosizeexa">GetFileVersionInfoSizeEx</a> function before calling the <b>GetFileVersionInfoEx</b> function. To retrieve information from the file-version information buffer, use the <a href="/windows/desktop/api/winver/nf-winver-verqueryvaluea">VerQueryValue</a> function.
      





> [!NOTE]
> The winver.h header defines GetFileVersionInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winver/nf-winver-getfileversioninfoa">GetFileVersionInfo</a>



<a href="/windows/desktop/api/winver/nf-winver-getfileversioninfosizeexa">GetFileVersionInfoSizeEx</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/vs-versioninfo">VS_VERSIONINFO</a>



<a href="/windows/desktop/api/winver/nf-winver-verqueryvaluea">VerQueryValue</a>



<a href="/windows/desktop/menurc/version-information">Version Information</a>
