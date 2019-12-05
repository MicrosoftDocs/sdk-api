---
UID: NF:winver.GetFileVersionInfoSizeA
title: GetFileVersionInfoSizeA function (winver.h)
description: Determines whether the operating system can retrieve version information for a specified file. If version information is available, GetFileVersionInfoSize returns the size, in bytes, of that information.
old-location: menurc\getfileversioninfosize.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\versioninformation\versioninformationreference\versioninformationfunctions\getfileversioninfosize.htm
ms.date: 12/05/2018
ms.keywords: GetFileVersionInfoSize, GetFileVersionInfoSize function [Menus and Other Resources], GetFileVersionInfoSizeA, GetFileVersionInfoSizeW, _win32_GetFileVersionInfoSize, _win32_getfileversioninfosize_cpp, menurc.getfileversioninfosize, winui._win32_getfileversioninfosize, winver/GetFileVersionInfoSize, winver/GetFileVersionInfoSizeA, winver/GetFileVersionInfoSizeW
ms.topic: function
f1_keywords:
- winver/GetFileVersionInfoSize
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetFileVersionInfoSizeA function


## -description


Determines whether the operating system can retrieve version information for a specified file. If version information is available, <b>GetFileVersionInfoSize</b> returns the size, in bytes, of that information. 


## -parameters




### -param lptstrFilename [in]

Type: <b>LPCTSTR</b>

The name of the file of interest. The function uses the search sequence specified by the  <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function.
				


### -param lpdwHandle [out, optional]

Type: <b>LPDWORD</b>

A pointer to a variable that the function sets to zero.


## -returns



Type: <b>DWORD</b>

If the function succeeds, the return value is the size, in bytes, of the file's version information.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



Call the 
				<b>GetFileVersionInfoSize</b> function before calling the <a href="https://docs.microsoft.com/windows/desktop/api/winver/nf-winver-getfileversioninfoa">GetFileVersionInfo</a> function. The size returned by <b>GetFileVersionInfoSize</b> indicates the buffer size required for the version information returned by <b>GetFileVersionInfo</b>. 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winver/nf-winver-getfileversioninfoa">GetFileVersionInfo</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/vs-versioninfo">VS_VERSIONINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winver/nf-winver-verqueryvaluea">VerQueryValue</a>



<a href="https://docs.microsoft.com/windows/desktop/menurc/version-information">Version Information</a>
 

 

