---
UID: NF:winbase.GetBinaryTypeA
title: GetBinaryTypeA function
author: windows-sdk-content
description: Determines whether a file is an executable (.exe) file, and if so, which subsystem runs the executable file.
old-location: fs\getbinarytype.htm
old-project: FileIO
ms.assetid: ec937372-ee99-4505-a5dd-7c111405cbc6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetBinaryType, GetBinaryType function [Files], GetBinaryTypeA, GetBinaryTypeW, SCS_32BIT_BINARY, SCS_64BIT_BINARY, SCS_DOS_BINARY, SCS_OS216_BINARY, SCS_PIF_BINARY, SCS_POSIX_BINARY, SCS_WOW_BINARY, _win32_getbinarytype, base.getbinarytype, fs.getbinarytype, winbase/GetBinaryType, winbase/GetBinaryTypeA, winbase/GetBinaryTypeW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetBinaryTypeA function


## -description


Determines whether a file is an executable (.exe) file, and if so, which subsystem runs the executable 
    file.


## -parameters




### -param lpApplicationName [in]

The full path of the file whose executable type is to be determined.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.


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
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the file is a DLL, 
       the last error code is <b>ERROR_BAD_EXE_FORMAT</b>.




## -remarks



As an alternative, you can obtain the same information by calling the 
    <a href="https://msdn.microsoft.com/d662bedf-4be0-4528-8121-e7923a42bc67">SHGetFileInfo</a> function, passing the 
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
 




## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/d662bedf-4be0-4528-8121-e7923a42bc67">SHGetFileInfo</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>
 

 

