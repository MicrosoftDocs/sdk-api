---
UID: NF:winbase.GetBinaryTypeW
title: GetBinaryTypeW function (winbase.h)
description: Determines whether a file is an executable (.exe) file, and if so, which subsystem runs the executable file. (Unicode)
helpviewer_keywords: ["GetBinaryType", "GetBinaryType function [Files]", "GetBinaryTypeW", "SCS_32BIT_BINARY", "SCS_64BIT_BINARY", "SCS_DOS_BINARY", "SCS_OS216_BINARY", "SCS_PIF_BINARY", "SCS_POSIX_BINARY", "SCS_WOW_BINARY", "_win32_getbinarytype", "base.getbinarytype", "fs.getbinarytype", "winbase/GetBinaryType", "winbase/GetBinaryTypeW"]
old-location: fs\getbinarytype.htm
tech.root: fs
ms.assetid: ec937372-ee99-4505-a5dd-7c111405cbc6
ms.date: 12/05/2018
ms.keywords: GetBinaryType, GetBinaryType function [Files], GetBinaryTypeA, GetBinaryTypeW, SCS_32BIT_BINARY, SCS_64BIT_BINARY, SCS_DOS_BINARY, SCS_OS216_BINARY, SCS_PIF_BINARY, SCS_POSIX_BINARY, SCS_WOW_BINARY, _win32_getbinarytype, base.getbinarytype, fs.getbinarytype, winbase/GetBinaryType, winbase/GetBinaryTypeA, winbase/GetBinaryTypeW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetBinaryTypeW (Unicode) and GetBinaryTypeA (ANSI)
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
 - GetBinaryTypeW
 - winbase/GetBinaryTypeW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetBinaryType
 - GetBinaryTypeA
 - GetBinaryTypeW
---

# GetBinaryTypeW function


## -description

Determines whether a file is an executable (.exe) file, and if so, which subsystem runs the executable 
    file.

## -parameters

### -param lpApplicationName [in]

The full path of the file whose executable type is to be determined.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpBinaryType [out]

A pointer to a variable to receive information about the executable type of the file specified by 
      <i>lpApplicationName</i>. The following constants are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCS_32BIT_BINARY"></a><a id="scs_32bit_binary"></a><dl>
<dt><b>SCS_32BIT_BINARY</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
A 32-bit Windows-based application

</td>
</tr>
<tr>
<td width="40%"><a id="SCS_64BIT_BINARY"></a><a id="scs_64bit_binary"></a><dl>
<dt><b>SCS_64BIT_BINARY</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
A 64-bit Windows-based application.

</td>
</tr>
<tr>
<td width="40%"><a id="SCS_DOS_BINARY"></a><a id="scs_dos_binary"></a><dl>
<dt><b>SCS_DOS_BINARY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
An MS-DOS – based application

</td>
</tr>
<tr>
<td width="40%"><a id="SCS_OS216_BINARY"></a><a id="scs_os216_binary"></a><dl>
<dt><b>SCS_OS216_BINARY</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
A 16-bit OS/2-based application

</td>
</tr>
<tr>
<td width="40%"><a id="SCS_PIF_BINARY"></a><a id="scs_pif_binary"></a><dl>
<dt><b>SCS_PIF_BINARY</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
A PIF file that executes an MS-DOS – based application

</td>
</tr>
<tr>
<td width="40%"><a id="SCS_POSIX_BINARY"></a><a id="scs_posix_binary"></a><dl>
<dt><b>SCS_POSIX_BINARY</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
A POSIX – based application

</td>
</tr>
<tr>
<td width="40%"><a id="SCS_WOW_BINARY"></a><a id="scs_wow_binary"></a><dl>
<dt><b>SCS_WOW_BINARY</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
A 16-bit Windows-based application

</td>
</tr>
</table>

## -returns

If the file is executable, the return value is nonzero. The function sets the variable pointed to by 
       <i>lpBinaryType</i> to indicate the file's executable type.

If the file is not executable, or if the function fails, the return value is zero. To get extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the file is a DLL, 
       the last error code is <b>ERROR_BAD_EXE_FORMAT</b>.

## -remarks

As an alternative, you can obtain the same information by calling the 
    <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetfileinfoa">SHGetFileInfo</a> function, passing the 
    <b>SHGFI_EXETYPE</b> flag in the <i>uFlags</i> parameter.

Symbolic link behavior—If the path points to a symbolic link, the target file is 
    used.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 





> [!NOTE]
> The winbase.h header defines GetBinaryType as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-shgetfileinfoa">SHGetFileInfo</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>
