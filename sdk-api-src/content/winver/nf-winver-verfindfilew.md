---
UID: NF:winver.VerFindFileW
title: VerFindFileW function (winver.h)
description: Determines where to install a file based on whether it locates another version of the file in the system. The values VerFindFile returns in the specified buffers are used in a subsequent call to the VerInstallFile function. (Unicode)
helpviewer_keywords: ["VFFF_ISSHAREDFILE", "VerFindFile", "VerFindFile function [Menus and Other Resources]", "VerFindFileW", "_win32_VerFindFile", "_win32_verfindfile_cpp", "menurc.verfindfile", "winui._win32_verfindfile", "winver/VerFindFile", "winver/VerFindFileW"]
old-location: menurc\verfindfile.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\versioninformation\versioninformationreference\versioninformationfunctions\verfindfile.htm
ms.date: 12/05/2018
ms.keywords: VFFF_ISSHAREDFILE, VerFindFile, VerFindFile function [Menus and Other Resources], VerFindFileA, VerFindFileW, _win32_VerFindFile, _win32_verfindfile_cpp, menurc.verfindfile, winui._win32_verfindfile, winver/VerFindFile, winver/VerFindFileA, winver/VerFindFileW
req.header: winver.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: VerFindFileW (Unicode) and VerFindFileA (ANSI)
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
 - VerFindFileW
 - winver/VerFindFileW
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
api_name:
 - VerFindFile
 - VerFindFileA
 - VerFindFileW
---

# VerFindFileW function


## -description

Determines where to install a file based on whether it locates another version of the file in the system. The values <b>VerFindFile</b> returns in the specified buffers are used in a subsequent call to the <a href="/windows/desktop/api/winver/nf-winver-verinstallfilea">VerInstallFile</a> function.

## -parameters

### -param uFlags [in]

Type: <b>DWORD</b>

This parameter can be the following value. All other bits are reserved. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VFFF_ISSHAREDFILE"></a><a id="vfff_issharedfile"></a><dl>
<dt><b>VFFF_ISSHAREDFILE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The source file can be shared by multiple applications. An application can use this information to determine where the file should be copied.

</td>
</tr>
</table>

### -param szFileName [in]

Type: <b>LPCTSTR</b>

The name of the file to be installed. Include only the file name and extension, not a path.

### -param szWinDir [in, optional]

Type: <b>LPCTSTR</b>

The directory in which Windows is running or will be run. This string is returned by the  <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a> function.

### -param szAppDir [in]

Type: <b>LPCTSTR</b>

The directory where the installation program is installing a set of related files. If the installation program is installing an application, this is the directory where the application will reside. This parameter also points to the application's current directory unless otherwise specified.

### -param szCurDir [out]

Type: <b>LPWSTR</b>

A buffer that receives the path to a current version of the file being installed. The path is a zero-terminated string. If a current version is not installed, the buffer will contain a zero-length string. The buffer should be at least <b>_MAX_PATH</b> characters long, although this is not required.

### -param puCurDirLen [in, out]

Type: <b>PUINT</b>

The length of the 
					<i>szCurDir</i>  buffer. This pointer must not be <b>NULL</b>.

When the function returns, 
					<i>lpuCurDirLen</i> contains the size, in characters, of the data returned in 
					<i>szCurDir</i>, including the terminating null character. If the buffer is too small to contain all the data, 
					<i>lpuCurDirLen</i> will be the size of the buffer required to hold the path.

### -param szDestDir [out]

Type: <b>LPTSTR</b>

A buffer that receives the path to the installation location recommended by <b>VerFindFile</b>. The path is a zero-terminated string. The buffer should be at least <b>_MAX_PATH</b> characters long, although this is not required.

### -param puDestDirLen [in, out]

Type: <b>PUINT</b>

A pointer to a variable that specifies the length of the 
					<i>szDestDir</i> buffer. This pointer must not be <b>NULL</b>.

When the function returns, 
					<i>lpuDestDirLen</i> contains the size, in characters, of the data returned in 
					<i>szDestDir</i>, including the terminating null character. If the buffer is too small to contain all the data, 
					<i>lpuDestDirLen</i> will be the size of the buffer needed to hold the path.

## -returns

Type: <b>DWORD</b>

The return value is a bitmask that indicates the status of the file. It can be one or more of the following values. All other values are reserved.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFF_CURNEDEST</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The currently installed version of the file is not in the recommended destination.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFF_FILEINUSE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The system is using the currently installed version of the file; therefore, the file cannot be overwritten or deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFF_BUFFTOOSMALL</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
At least one of the buffers was too small to contain the corresponding string. An application should check the output buffers to determine which buffer was too small.

</td>
</tr>
</table>

## -remarks

This function works on 16-, 32-, and 64-bit file images.

<b>VerFindFile</b> searches for a copy of the specified file by using the <a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a>   function. However, it determines the system directory from the specified Windows directory, or searches the path. 

If the 
				<i>dwFlags</i> parameter indicates that the file is private to this application (not <b>VFFF_ISSHAREDFILE</b>), <b>VerFindFile</b> recommends installing the file in the application's directory. Otherwise, if the system is running a shared copy of the system, the function recommends installing the file in the Windows directory. If the system is running a private copy of the system, the function recommends installing the file in the system directory. 





> [!NOTE]
> The winver.h header defines VerFindFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winver/nf-winver-verinstallfilea">VerInstallFile</a>



<a href="/windows/desktop/menurc/version-information">Version Information</a>
