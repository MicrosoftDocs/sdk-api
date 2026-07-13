---
UID: NF:winver.GetFileVersionInfoSizeExA
title: GetFileVersionInfoSizeExA function (winver.h)
description: Determines whether the operating system can retrieve version information for a specified file. If version information is available, GetFileVersionInfoSizeEx returns the size, in bytes, of that information. (ANSI)
helpviewer_keywords: ["FILE_VER_GET_LOCALISED", "FILE_VER_GET_NEUTRAL", "GetFileVersionInfoSizeExA", "winver/GetFileVersionInfoSizeExA"]
old-location: menurc\getfileversioninfosizeex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\versioninformation\versioninformationreference\versioninformationfunctions\getfileversioninfosizeex.htm
ms.date: 12/05/2018
ms.keywords: FILE_VER_GET_LOCALISED, FILE_VER_GET_NEUTRAL, GetFileVersionInfoSizeEx, GetFileVersionInfoSizeEx function [Menus and Other Resources], GetFileVersionInfoSizeExA, GetFileVersionInfoSizeExW, _win32_GetFileVersionInfoSizeEx, _win32_getfileversioninfosizeex_cpp, menurc.getfileversioninfosizeex, winui._win32_getfileversioninfosizeex, winver/GetFileVersionInfoSizeEx, winver/GetFileVersionInfoSizeExA, winver/GetFileVersionInfoSizeExW
req.header: winver.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFileVersionInfoSizeExW (Unicode) and GetFileVersionInfoSizeExA (ANSI)
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
 - GetFileVersionInfoSizeExA
 - winver/GetFileVersionInfoSizeExA
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
 - GetFileVersionInfoSizeEx
 - GetFileVersionInfoSizeExA
 - GetFileVersionInfoSizeExW
---

# GetFileVersionInfoSizeExA function


## -description

Determines whether the operating system can retrieve version information for a specified file. If version information is available, <b>GetFileVersionInfoSizeEx</b> returns the size, in bytes, of that information.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

Controls which MUI DLLs (if any) from which the version resource is extracted. Zero or more of the following flags.

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
<dt>0x002</dt>
</dl>
</td>
<td width="60%">
Loads the version resource strings from the corresponding MUI file, if available, and loads the binary version information (<b>VS_FIXEDFILEINFO</b>) from the corresponding language-neutral file, if available. 

</td>
</tr>
</table>

### -param lpwstrFilename [in]

Type: <b>LPCTSTR</b>

The name of the file of interest. The function uses the search sequence specified by the  <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function.

### -param lpdwHandle [out, optional]

Type: <b>LPDWORD</b>

When this function returns, contains a pointer to a variable that is set to zero because this function sets it to zero. This parameter exists for historical reasons.

## -returns

Type: <b>DWORD</b>

If the function succeeds, the return value is the size, in bytes, of the file's version information.
                    
                    

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Call the <b>GetFileVersionInfoSizeEx</b> function before calling the <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfoexa">GetFileVersionInfoEx</a> function. The size returned by <b>GetFileVersionInfoSizeEx</b> indicates the buffer size required for the version information returned by <b>GetFileVersionInfoEx</b>.





> [!NOTE]
> The winver.h header defines GetFileVersionInfoSizeEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winver/nf-winver-getfileversioninfoexa">GetFileVersionInfoEx</a>



<a href="/windows/desktop/api/winver/nf-winver-getfileversioninfosizea">GetFileVersionInfoSize</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/vs-versioninfo">VS_VERSIONINFO</a>



<a href="/windows/desktop/api/winver/nf-winver-verqueryvaluea">VerQueryValue</a>



<a href="/windows/desktop/menurc/version-information">Version Information</a>
