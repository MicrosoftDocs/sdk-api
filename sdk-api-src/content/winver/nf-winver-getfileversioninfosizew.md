---
UID: NF:winver.GetFileVersionInfoSizeW
title: GetFileVersionInfoSizeW function (winver.h)
description: Determines whether the operating system can retrieve version information for a specified file. If version information is available, GetFileVersionInfoSize returns the size, in bytes, of that information. (Unicode)
helpviewer_keywords: ["GetFileVersionInfoSize", "GetFileVersionInfoSize function [Menus and Other Resources]", "GetFileVersionInfoSizeW", "_win32_GetFileVersionInfoSize", "_win32_getfileversioninfosize_cpp", "menurc.getfileversioninfosize", "winui._win32_getfileversioninfosize", "winver/GetFileVersionInfoSize", "winver/GetFileVersionInfoSizeW"]
old-location: menurc\getfileversioninfosize.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\versioninformation\versioninformationreference\versioninformationfunctions\getfileversioninfosize.htm
ms.date: 12/05/2018
ms.keywords: GetFileVersionInfoSize, GetFileVersionInfoSize function [Menus and Other Resources], GetFileVersionInfoSizeA, GetFileVersionInfoSizeW, _win32_GetFileVersionInfoSize, _win32_getfileversioninfosize_cpp, menurc.getfileversioninfosize, winui._win32_getfileversioninfosize, winver/GetFileVersionInfoSize, winver/GetFileVersionInfoSizeA, winver/GetFileVersionInfoSizeW
req.header: winver.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFileVersionInfoSizeW (Unicode) and GetFileVersionInfoSizeA (ANSI)
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
 - GetFileVersionInfoSizeW
 - winver/GetFileVersionInfoSizeW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-version-l1-1-0.dll
 - API-MS-Win-Core-Versionansi-L1-1-1.dll
 - API-MS-Win-Core-Version-L1-1-1.dll
 - KernelBase.dll
 - version.dll
api_name:
 - GetFileVersionInfoSize
 - GetFileVersionInfoSizeA
 - GetFileVersionInfoSizeW
---

# GetFileVersionInfoSizeW function


## -description

Determines whether the operating system can retrieve version information for a specified file. If version information is available, <b>GetFileVersionInfoSize</b> returns the size, in bytes, of that information.

## -parameters

### -param lptstrFilename [in]

Type: <b>LPCTSTR</b>

The name of the file of interest. The function uses the search sequence specified by the  <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function.

### -param lpdwHandle [out, optional]

Type: <b>LPDWORD</b>

A pointer to a variable that the function sets to zero.

## -returns

Type: <b>DWORD</b>

If the function succeeds, the return value is the size, in bytes, of the file's version information.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Call the 
				<b>GetFileVersionInfoSize</b> function before calling the <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfoa">GetFileVersionInfo</a> function. The size returned by <b>GetFileVersionInfoSize</b> indicates the buffer size required for the version information returned by <b>GetFileVersionInfo</b>. 





> [!NOTE]
> The winver.h header defines GetFileVersionInfoSize as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winver/nf-winver-getfileversioninfoa">GetFileVersionInfo</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/vs-versioninfo">VS_VERSIONINFO</a>



<a href="/windows/desktop/api/winver/nf-winver-verqueryvaluea">VerQueryValue</a>



<a href="/windows/desktop/menurc/version-information">Version Information</a>
