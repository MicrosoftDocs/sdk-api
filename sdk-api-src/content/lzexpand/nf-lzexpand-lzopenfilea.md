---
UID: NF:lzexpand.LZOpenFileA
title: LZOpenFileA function (lzexpand.h)
description: Creates, opens, reopens, or deletes the specified file. (ANSI)
helpviewer_keywords: ["LZOpenFileA", "OF_CANCEL", "OF_CREATE", "OF_DELETE", "OF_EXIST", "OF_PARSE", "OF_PROMPT", "OF_READ", "OF_READWRITE", "OF_REOPEN", "OF_SHARE_DENY_NONE", "OF_SHARE_DENY_READ", "OF_SHARE_DENY_WRITE", "OF_SHARE_EXCLUSIVE", "OF_WRITE", "lzexpand/LZOpenFileA"]
old-location: fs\lzopenfile.htm
tech.root: fs
ms.assetid: 6ab3c81c-88f2-4b87-84b1-5b64848af043
ms.date: 12/05/2018
ms.keywords: LZOpenFile, LZOpenFile function [Files], LZOpenFileA, LZOpenFileW, OF_CANCEL, OF_CREATE, OF_DELETE, OF_EXIST, OF_PARSE, OF_PROMPT, OF_READ, OF_READWRITE, OF_REOPEN, OF_SHARE_DENY_NONE, OF_SHARE_DENY_READ, OF_SHARE_DENY_WRITE, OF_SHARE_EXCLUSIVE, OF_WRITE, _win32_lzopenfile, base.lzopenfile, fs.lzopenfile, lzexpand/LZOpenFile, lzexpand/LZOpenFileA, lzexpand/LZOpenFileW
req.header: lzexpand.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LZOpenFileW (Unicode) and LZOpenFileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Lz32.lib
req.dll: Lz32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LZOpenFileA
 - lzexpand/LZOpenFileA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Lz32.dll
api_name:
 - LZOpenFile
 - LZOpenFileA
 - LZOpenFileW
---

# LZOpenFileA function


## -description

Creates, opens, reopens, or deletes the specified file.

## -parameters

### -param lpFileName [in]

The name of the file.

### -param lpReOpenBuf [out]

A pointer to the <a href="/windows/desktop/api/winbase/ns-winbase-ofstruct">OFSTRUCT</a> structure that is to receive 
       information about the file when the file is first opened. The structure can be used in subsequent calls to the 
       <b>LZOpenFile</b> function to see the open file.

The <b>szPathName</b> member of this structure contains characters from the original 
       equipment manufacturer (OEM) character set.

### -param wStyle [in]

The action to be taken. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OF_CANCEL"></a><a id="of_cancel"></a><dl>
<dt><b>OF_CANCEL</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
Ignored. Provided only for compatibility with 16-bit Windows. Use the <b>OF_PROMPT</b> 
        style to display a dialog box containing a <b>Cancel</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_CREATE"></a><a id="of_create"></a><dl>
<dt><b>OF_CREATE</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Directs <b>LZOpenFile</b> to create a new file. If the file already exists, it 
        is truncated to zero length.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_DELETE"></a><a id="of_delete"></a><dl>
<dt><b>OF_DELETE</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Deletes the file.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_EXIST"></a><a id="of_exist"></a><dl>
<dt><b>OF_EXIST</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
Opens the file and then closes it to test for a file's existence.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_PARSE"></a><a id="of_parse"></a><dl>
<dt><b>OF_PARSE</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Fills the <a href="/windows/desktop/api/winbase/ns-winbase-ofstruct">OFSTRUCT</a> structure but carries out no 
        other action.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_PROMPT"></a><a id="of_prompt"></a><dl>
<dt><b>OF_PROMPT</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
Displays a dialog box if the requested file does not exist. The dialog box informs the user that the 
        system cannot find the file, and it contains <b>Retry</b> and 
        <b>Cancel</b> buttons. Clicking the <b>Cancel</b> button directs 
        <b>LZOpenFile</b> to return a file not found error message.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_READ"></a><a id="of_read"></a><dl>
<dt><b>OF_READ</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Opens the file for reading only.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_READWRITE"></a><a id="of_readwrite"></a><dl>
<dt><b>OF_READWRITE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Opens the file for reading and writing.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_REOPEN"></a><a id="of_reopen"></a><dl>
<dt><b>OF_REOPEN</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
Opens the file using information in the reopen buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_SHARE_DENY_NONE"></a><a id="of_share_deny_none"></a><dl>
<dt><b>OF_SHARE_DENY_NONE</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Opens the file without denying other processes read or write access to the file. 
        <b>LZOpenFile</b> fails if the file has been opened in compatibility mode by any 
        other process.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_SHARE_DENY_READ"></a><a id="of_share_deny_read"></a><dl>
<dt><b>OF_SHARE_DENY_READ</b></dt>
<dt>0x0030</dt>
</dl>
</td>
<td width="60%">
Opens the file and denies other processes read access to the file. 
        <b>LZOpenFile</b> fails if the file has been opened in compatibility mode or has 
        been opened for read access by any other process.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_SHARE_DENY_WRITE"></a><a id="of_share_deny_write"></a><dl>
<dt><b>OF_SHARE_DENY_WRITE</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Opens the file and denies other processes write access to the file. 
        <b>LZOpenFile</b> fails if the file has been opened in compatibility mode or has 
        been opened for write access by any other process.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_SHARE_EXCLUSIVE"></a><a id="of_share_exclusive"></a><dl>
<dt><b>OF_SHARE_EXCLUSIVE</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Opens the file in exclusive mode, denying other processes both read and write access to the file. 
        <b>LZOpenFile</b> fails if the file has been opened in any other mode for read or 
        write access, even by the current process.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_WRITE"></a><a id="of_write"></a><dl>
<dt><b>OF_WRITE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Opens the file for writing only.

</td>
</tr>
</table>

## -returns

If the function succeeds and the value specified by the <i>wStyle</i> parameter is not 
       <b>OF_READ</b>, the return value is a handle identifying the file. If the file is compressed 
       and opened with <i>wStyle</i> set to <b>OF_READ</b>, the return value is 
       a special file handle.

If the function fails, the return value is an <b>LZERROR_*</b> code. These codes have 
       values less than zero. There is no extended error information for this function; do not call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  <b>LZOpenFile</b> calls neither 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> nor 
       <a href="/windows/desktop/api/winuser/nf-winuser-setlasterrorex">SetLastErrorEx</a>; thus, its failure does not affect a 
       thread's last-error code.</div>
<div> </div>
The following is the list of the error codes that <b>LZOpenFile</b> can return upon 
       failure.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LZERROR_BADINHANDLE</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The handle identifying the source file is not valid. The file cannot be read.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LZERROR_GLOBALLOC</b></dt>
<dt>-5</dt>
</dl>
</td>
<td width="60%">
The maximum number of open compressed files has been exceeded or local memory cannot be allocated.

</td>
</tr>
</table>

## -remarks

If the <i>wStyle</i> parameter is the <b>OF_READ</b> flag (or 
    <b>OF_READ</b> and any of the <b>OF_SHARE_*</b> flags) and the file is 
    compressed, <b>LZOpenFile</b> calls the 
    <a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzinit">LZInit</a> function, which performs the required initialization for 
    the decompression operations.

The handle this function returns is compatible only with the functions in Lz32.dll; it should not be used 
    for other file operations.

If <b>LZOpenFile</b> is unable to open the file specified by 
    <i>lpFileName</i>, on some versions of Windows it attempts to open a file with almost the same 
    file name, except the last character is replaced with an underscore ("_"). Thus, if an attempt to 
    open "MyProgram.exe" fails, <b>LZOpenFile</b> tries to open 
    "MyProgram.ex_". Installation packages often substitute the underscore for the last letter of a 
    file name extension to indicate that the file is compressed. For example, "MyProgram.exe" 
    compressed might be named "MyProgram.ex_". To determine the name of the file opened (if any), 
    examine the <b>szPathName</b> member of the 
    <a href="/windows/desktop/api/winbase/ns-winbase-ofstruct">OFSTRUCT</a> structure in the 
    <i>lpReOpenBuf</i> parameter.

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
 

CsvFs will do redirected IO for compressed files.






> [!NOTE]
> The lzexpand.h header defines LZOpenFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-compression-and-decompression">File Compression and Decompression</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzclose">LZClose</a>



<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzinit">LZInit</a>



<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzread">LZRead</a>



<a href="/windows/desktop/api/winbase/ns-winbase-ofstruct">OFSTRUCT</a>
