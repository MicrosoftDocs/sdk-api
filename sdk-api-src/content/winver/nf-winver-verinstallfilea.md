---
UID: NF:winver.VerInstallFileA
title: VerInstallFileA function (winver.h)
description: Installs the specified file based on information returned from the VerFindFile function. VerInstallFile decompresses the file, if necessary, assigns a unique filename, and checks for errors, such as outdated files. (ANSI)
helpviewer_keywords: ["VIFF_DONTDELETEOLD", "VIFF_FORCEINSTALL", "VerInstallFileA", "winver/VerInstallFileA"]
old-location: menurc\verinstallfile.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\versioninformation\versioninformationreference\versioninformationfunctions\verinstallfile.htm
ms.date: 12/05/2018
ms.keywords: VIFF_DONTDELETEOLD, VIFF_FORCEINSTALL, VerInstallFile, VerInstallFile function [Menus and Other Resources], VerInstallFileA, VerInstallFileW, _win32_VerInstallFile, _win32_verinstallfile_cpp, menurc.verinstallfile, winui._win32_verinstallfile, winver/VerInstallFile, winver/VerInstallFileA, winver/VerInstallFileW
req.header: winver.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: VerInstallFileW (Unicode) and VerInstallFileA (ANSI)
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
 - VerInstallFileA
 - winver/VerInstallFileA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-version-l1-1-0.dll
 - version.dll
api_name:
 - VerInstallFile
 - VerInstallFileA
 - VerInstallFileW
---

# VerInstallFileA function


## -description

Installs the specified file based on information returned from the <a href="/windows/desktop/api/winver/nf-winver-verfindfilea">VerFindFile</a> function. <b>VerInstallFile</b> decompresses the file, if necessary, assigns a unique filename, and checks for errors, such as outdated files.

## -parameters

### -param uFlags [in]

Type: <b>DWORD</b>

This parameter can be one of the following values. All other bits are reserved. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VIFF_FORCEINSTALL"></a><a id="viff_forceinstall"></a><dl>
<dt><b>VIFF_FORCEINSTALL</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Installs the file regardless of mismatched version numbers. The function checks only for physical errors during installation.

</td>
</tr>
<tr>
<td width="40%"><a id="VIFF_DONTDELETEOLD"></a><a id="viff_dontdeleteold"></a><dl>
<dt><b>VIFF_DONTDELETEOLD</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Installs the file without deleting the previously installed file, if the previously installed file is not in the destination directory.

</td>
</tr>
</table>

### -param szSrcFileName [in]

Type: <b>LPCTSTR</b>

The name of the file to be installed. This is the filename in the directory pointed to by the 
					<i>szSrcDir</i> parameter; the filename can include only the filename and extension, not a path.

### -param szDestFileName [in]

Type: <b>LPCTSTR</b>

The name <b>VerInstallFile</b> will give the new file upon installation. This file name may be different from the filename in the 
					<i>szSrcFileName</i> directory. The new name should include only the file name and extension, not a path.

### -param szSrcDir [in]

Type: <b>LPCTSTR</b>

The name of the directory where the file can be found.

### -param szDestDir [in]

Type: <b>LPCTSTR</b>

The name of the directory where the file should be installed. <a href="/windows/desktop/api/winver/nf-winver-verfindfilea">VerFindFile</a> returns this value in its 
					<i>szDestDir</i> parameter.

### -param szCurDir [in]

Type: <b>LPCTSTR</b>

The name of the directory where a preexisting version of this file can be found. <a href="/windows/desktop/api/winver/nf-winver-verfindfilea">VerFindFile</a> returns this value in its 
					<i>szCurDir</i> parameter.

### -param szTmpFile [out]

Type: <b>LPTSTR</b>

The name of a temporary copy of the source file. The buffer should be at least <b>_MAX_PATH</b> characters long, although this is not required, and should be empty on input.

### -param puTmpFileLen [in, out]

Type: <b>PUINT</b>

The length of the 
					<i>szTmpFile</i> buffer. This pointer must not be <b>NULL</b>.

When the function returns, 
					<i>lpuTmpFileLen</i> receives the size, in characters, of the data returned in 
					<i>szTmpFile</i>, including the terminating null character. If the buffer is too small to contain all the data, 
					<i>lpuTmpFileLen</i> will be the size of the buffer required to hold the data.

## -returns

Type: <b>DWORD</b>

The return value is a bitmask that indicates exceptions. It can be one or more of the following values. All other values are reserved.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_ACCESSVIOLATION</b></dt>
<dt>0x00000200L</dt>
</dl>
</td>
<td width="60%">
A read, create, delete, or rename operation failed due to an access violation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_BUFFTOOSMALL</b></dt>
<dt>0x00040000L</dt>
</dl>
</td>
<td width="60%">
The <i>szTmpFile</i> buffer was too small to contain the name of the temporary source file. When the function returns, <i>lpuTmpFileLen</i> contains the size of the buffer required to hold the filename.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_CANNOTCREATE</b></dt>
<dt>0x00000800L</dt>
</dl>
</td>
<td width="60%">
The function cannot create the temporary file. The specific error may be described by another flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_CANNOTDELETE</b></dt>
<dt>0x00001000L</dt>
</dl>
</td>
<td width="60%">
The function cannot delete the destination file, or cannot delete the existing version of the file located in another directory. If the <b>VIF_TEMPFILE</b> bit is set, the installation failed, and the destination file probably cannot be deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_CANNOTDELETECUR</b></dt>
<dt>0x00004000L</dt>
</dl>
</td>
<td width="60%">
The existing version of the file could not be deleted and <b>VIFF_DONTDELETEOLD</b> was not specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_CANNOTLOADCABINET</b></dt>
<dt>0x00100000L</dt>
</dl>
</td>
<td width="60%">
The function cannot load the cabinet file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_CANNOTLOADLZ32</b></dt>
<dt>0x00080000L</dt>
</dl>
</td>
<td width="60%">
The function cannot load the compressed file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_CANNOTREADDST</b></dt>
<dt>0x00020000L</dt>
</dl>
</td>
<td width="60%">
The function cannot read the destination (existing) files. This prevents the function from examining the file's attributes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_CANNOTREADSRC</b></dt>
<dt>0x00010000L</dt>
</dl>
</td>
<td width="60%">
The function cannot read the source file. This could mean that the path was not specified properly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_CANNOTRENAME</b></dt>
<dt>0x00002000L</dt>
</dl>
</td>
<td width="60%">
The function cannot rename the temporary file, but already deleted the destination file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_DIFFCODEPG</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td width="60%">
The new file requires a code page that cannot be displayed by the version of the system currently running. This error can be overridden by calling <a href="/windows/desktop/api/winver/nf-winver-verinstallfilea">VerInstallFile</a> with the <b>VIFF_FORCEINSTALL</b> flag set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_DIFFLANG</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
The new and preexisting files have different language or code-page values. This error can be overridden by calling <a href="/windows/desktop/api/winver/nf-winver-verinstallfilea">VerInstallFile</a> again with the <b>VIFF_FORCEINSTALL</b> flag set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_DIFFTYPE</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
The new file has a different type, subtype, or operating system from the preexisting file. This error can be overridden by calling <a href="/windows/desktop/api/winver/nf-winver-verinstallfilea">VerInstallFile</a> again with the <b>VIFF_FORCEINSTALL</b> flag set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_FILEINUSE</b></dt>
<dt>0x00000080L</dt>
</dl>
</td>
<td width="60%">
The preexisting file is in use by the system and cannot be deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_MISMATCH</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
The new and preexisting files differ in one or more attributes. This error can be overridden by calling <a href="/windows/desktop/api/winver/nf-winver-verinstallfilea">VerInstallFile</a> again with the <b>VIFF_FORCEINSTALL</b> flag set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_OUTOFMEMORY</b></dt>
<dt>0x00008000L</dt>
</dl>
</td>
<td width="60%">
The function cannot complete the requested operation due to insufficient memory. Generally, this means the application ran out of memory attempting to expand a compressed file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_OUTOFSPACE</b></dt>
<dt>0x00000100L</dt>
</dl>
</td>
<td width="60%">
The function cannot create the temporary file due to insufficient disk space on the destination drive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_SHARINGVIOLATION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
A read, create, delete, or rename operation failed due to a sharing violation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_SRCOLD</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
The file to install is older than the preexisting file. This error can be overridden by calling <a href="/windows/desktop/api/winver/nf-winver-verinstallfilea">VerInstallFile</a> again with the <b>VIFF_FORCEINSTALL</b> flag set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_TEMPFILE</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
The temporary copy of the new file is in the destination directory. The cause of failure is reflected in other flags.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIF_WRITEPROT</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td width="60%">
The preexisting file is write-protected. This error can be overridden by calling <a href="/windows/desktop/api/winver/nf-winver-verinstallfilea">VerInstallFile</a> again with the <b>VIFF_FORCEINSTALL</b> flag set.

</td>
</tr>
</table>

## -remarks

This function works on 16-, 32-, and 64-bit file images.

<b>VerInstallFile</b> copies the file from the source directory to the destination directory. If 
				<i>szCurDir</i> indicates that a previous version of the file exists on the system, <b>VerInstallFile</b> compares the files' version stamp information. If the previously installed version of the file is more recent than the new version, or if the files' attributes are significantly different, for example, if they are in different languages, then <b>VerInstallFile</b> returns with one or more recoverable error codes. 

<b>VerInstallFile</b> leaves the temporary file in the destination directory. The application can either override the error or delete the temporary file. If the application overrides the error, <b>VerInstallFile</b> deletes the previously installed version and renames the temporary file with the original filename. 





> [!NOTE]
> The winver.h header defines VerInstallFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winver/nf-winver-verfindfilea">VerFindFile</a>



<a href="/windows/desktop/menurc/version-information">Version Information</a>
