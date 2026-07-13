---
UID: NF:winver.GetFileVersionInfoW
title: GetFileVersionInfoW function (winver.h)
description: Retrieves version information for the specified file. (GetFileVersionInfoW)
helpviewer_keywords: ["GetFileVersionInfo", "GetFileVersionInfo function [Menus and Other Resources]", "GetFileVersionInfoW", "_win32_GetFileVersionInfo", "_win32_getfileversioninfo_cpp", "menurc.getfileversioninfo", "winui._win32_getfileversioninfo", "winver/GetFileVersionInfo", "winver/GetFileVersionInfoW"]
old-location: menurc\getfileversioninfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\versioninformation\versioninformationreference\versioninformationfunctions\getfileversioninfo.htm
ms.date: 12/05/2018
ms.keywords: GetFileVersionInfo, GetFileVersionInfo function [Menus and Other Resources], GetFileVersionInfoA, GetFileVersionInfoW, _win32_GetFileVersionInfo, _win32_getfileversioninfo_cpp, menurc.getfileversioninfo, winui._win32_getfileversioninfo, winver/GetFileVersionInfo, winver/GetFileVersionInfoA, winver/GetFileVersionInfoW
req.header: winver.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFileVersionInfoW (Unicode) and GetFileVersionInfoA (ANSI)
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
 - GetFileVersionInfoW
 - winver/GetFileVersionInfoW
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
 - GetFileVersionInfo
 - GetFileVersionInfoA
 - GetFileVersionInfoW
---

# GetFileVersionInfoW function


## -description

Retrieves version information for the specified file.

## -parameters

### -param lptstrFilename [in]

Type: <b>LPCTSTR</b>

The name of the file. If a full path is not specified, the function uses the search sequence specified by the  <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function.

### -param dwHandle

Type: <b>DWORD</b>

This parameter is ignored.

### -param dwLen [in]

Type: <b>DWORD</b>

The size, in bytes, of the buffer pointed to by the 
					<i>lpData</i> parameter. 

Call the <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfosizea">GetFileVersionInfoSize</a> function first to determine the size, in bytes, of a file's version information. The 
						<i>dwLen</i> member should be equal to or greater than that value. 

If the buffer pointed to by 
						<i>lpData</i> is not large enough, the function truncates the file's version information to the size of the buffer.

### -param lpData [out]

Type: <b>LPVOID</b>

Pointer to a buffer that receives the file-version information.

You can use this value in a subsequent call to the <a href="/windows/desktop/api/winver/nf-winver-verqueryvaluea">VerQueryValue</a> function to retrieve data from the buffer.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

 File version info has fixed and non-fixed part. The fixed part contains information like version number. The non-fixed part contains things like strings. In the past <b>GetFileVersionInfo</b> was taking version information from the binary (exe/dll). Currently, it is querying fixed version from language neutral file (exe/dll) and the non-fixed part from mui file, merges them and returns to the user.
If the given binary does not have a mui file then behavior is as in previous version.

Call the <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfosizea">GetFileVersionInfoSize</a> function before calling the <b>GetFileVersionInfo</b> function. To retrieve information from the file-version information buffer, use the <a href="/windows/desktop/api/winver/nf-winver-verqueryvaluea">VerQueryValue</a> function.





> [!NOTE]
> The winver.h header defines GetFileVersionInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winver/nf-winver-getfileversioninfosizea">GetFileVersionInfoSize</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/vs-versioninfo">VS_VERSIONINFO</a>



<a href="/windows/desktop/api/winver/nf-winver-verqueryvaluea">VerQueryValue</a>



<a href="/windows/desktop/menurc/version-information">Version Information</a>
