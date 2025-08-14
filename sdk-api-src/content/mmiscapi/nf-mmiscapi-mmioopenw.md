---
UID: NF:mmiscapi.mmioOpenW
title: mmioOpenW function (mmiscapi.h)
description: The mmioOpenW (Unicode) function opens a file for unbuffered or buffered I/O; creates a file; deletes a file; or checks whether a file exists. (mmioOpenW)
helpviewer_keywords: ["_win32_mmioOpen", "mmioOpen", "mmioOpen function [Windows Multimedia]", "mmioOpenW", "multimedia.mmioopen"]
old-location: multimedia\mmioopen.htm
tech.root: Multimedia
ms.assetid: 7361f0f2-1c3c-49f1-aec1-2927e05ef0f0
ms.date: 08/02/2022
ms.keywords: _win32_mmioOpen, mmioOpen, mmioOpen function [Windows Multimedia], mmioOpenA, mmioOpenW, mmsystem/mmioOpen, mmsystem/mmioOpenA, mmsystem/mmioOpenW, multimedia.mmioopen
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: mmioOpenW (Unicode) and mmioOpenA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mmioOpenW
 - mmiscapi/mmioOpenW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-mm-io-l1-1-0.dll
 - Winmm.dll
 - API-MS-Win-mm-misc-l1-1-0.dll
 - winmmbase.dll
 - API-MS-Win-mm-misc-l1-1-1.dll
api_name:
 - mmioOpen
 - mmioOpenA
 - mmioOpenW
---

# mmioOpenW function


## -description

The <b>mmioOpen</b> function opens a file for unbuffered or buffered I/O; creates a file; deletes a file; or checks whether a file exists. The file can be a standard file, a memory file, or an element of a custom storage system. The handle returned by <a href="/windows/desktop/Multimedia/opening-a-file-with-mmioopen">mmioOpen</a> is not a standard file handle; do not use it with any file I/O functions other than multimedia file I/O functions.

<div class="alert"><b>Note</b>  This function is deprecated. Applications should call <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> to create or open files.</div>
<div> </div>

## -parameters

### -param pszFileName

Pointer to a buffer that contains the name of the file. If no I/O procedure is specified to open the file, the file name determines how the file is opened, as follows:

<ul>
<li>If the file name does not contain a plus sign (+), it is assumed to be the name of a standard file (that is, a file whose type is not <b>HMMIO</b>).</li>
<li>If the file name is of the form EXAMPLE.EXT+ABC, the extension EXT is assumed to identify an installed I/O procedure which is called to perform I/O on the file. For more information, see <a href="/previous-versions/dd757323(v=vs.85)">mmioInstallIOProc</a>.</li>
<li>If the file name is <b>NULL</b> and no I/O procedure is given, the <b>adwInfo</b> member of the <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure is assumed to be the standard (non-<b>HMMIO</b>) file handle of a currently open file.</li>
</ul>
The file name should not be longer than 128 characters, including the terminating NULL character.

When opening a memory file, set <i>szFilename</i> to <b>NULL</b>.

### -param pmmioinfo

Pointer to an <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure containing extra parameters used by <b>mmioOpen</b>. Unless you are opening a memory file, specifying the size of a buffer for buffered I/O, or specifying an uninstalled I/O procedure to open a file, this parameter should be <b>NULL</b>. If this parameter is not <b>NULL</b>, all unused members of the <b>MMIOINFO</b> structure it references must be set to zero, including the reserved members.

### -param fdwOpen

Flags for the open operation. The MMIO_READ, MMIO_WRITE, and MMIO_READWRITE flags are mutually exclusive – only one should be specified. The MMIO_COMPAT, MMIO_EXCLUSIVE, MMIO_DENYWRITE, MMIO_DENYREAD, and MMIO_DENYNONE flags are file-sharing flags. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MMIO_ALLOCBUF</td>
<td>Opens a file for buffered I/O. To allocate a buffer larger or smaller than the default buffer size (8K, defined as MMIO_DEFAULTBUFFER), set the <b>cchBuffer</b> member of the <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure to the desired buffer size. If <b>cchBuffer</b> is zero, the default buffer size is used. If you are providing your own I/O buffer, this flag should not be used.</td>
</tr>
<tr>
<td>MMIO_COMPAT</td>
<td>Opens the file with compatibility mode, allowing any process on a given machine to open the file any number of times. If the file has been opened with any of the other sharing modes, <b>mmioOpen</b> fails.</td>
</tr>
<tr>
<td>MMIO_CREATE</td>
<td>Creates a new file. If the file already exists, it is truncated to zero length. For memory files, this flag indicates the end of the file is initially at the start of the buffer.</td>
</tr>
<tr>
<td>MMIO_DELETE</td>
<td>Deletes a file. If this flag is specified, <i>szFilename</i> should not be <b>NULL</b>. The return value is <b>TRUE</b> (cast to <b>HMMIO</b>) if the file was deleted successfully or <b>FALSE</b> otherwise. Do not call the <a href="/previous-versions/dd757316(v=vs.85)">mmioClose</a> function for a file that has been deleted. If this flag is specified, all other flags that open files are ignored.</td>
</tr>
<tr>
<td>MMIO_DENYNONE</td>
<td>Opens the file without denying other processes read or write access to the file. If the file has been opened in compatibility mode by any other process, <b>mmioOpen</b> fails.</td>
</tr>
<tr>
<td>MMIO_DENYREAD</td>
<td>Opens the file and denies other processes read access to the file. If the file has been opened in compatibility mode or for read access by any other process, <b>mmioOpen</b> fails.</td>
</tr>
<tr>
<td>MMIO_DENYWRITE</td>
<td>Opens the file and denies other processes write access to the file. If the file has been opened in compatibility mode or for write access by any other process, <b>mmioOpen</b> fails.</td>
</tr>
<tr>
<td>MMIO_EXCLUSIVE</td>
<td>Opens the file and denies other processes read and write access to the file. If the file has been opened in any other mode for read or write access, even by the current process, <b>mmioOpen</b> fails.</td>
</tr>
<tr>
<td>MMIO_EXIST</td>
<td>Determines whether the specified file exists and creates a fully qualified file name from the path specified in <i>szFilename</i>. The return value is <b>TRUE</b> (cast to <b>HMMIO</b>) if the qualification was successful and the file exists or <b>FALSE</b> otherwise. The file is not opened, and the function does not return a valid multimedia file I/O file handle, so do not attempt to close the file.
<div class="alert"><b>Note</b>  Applications should call <b>GetFileAttributes</b>  or <b>GetFileAttributesEx</b> instead.</div>
<div> </div>


</td>
</tr>
<tr>
<td>MMIO_GETTEMP</td>
<td>
Creates a temporary file name, optionally using the parameters passed in <i>szFilename.</i> For example, you can specify "C:F" to create a temporary file residing on drive C, starting with letter "F". The resulting file name is copied to the buffer pointed to by <i>szFilename</i>.  The buffer must be large enough to hold at least 128 characters.

If the temporary file name was created successfully, the return value is <b>MMSYSERR_NOERROR</b> (cast to <b>HMMIO</b>). Otherwise, the return value is <b>MMIOERR_FILENOTFOUND</b> otherwise. The file is not opened, and the function does not return a valid multimedia file I/O file handle, so do not attempt to close the file. This flag overrides all other flags.


<div class="alert"><b>Note</b>  Applications should call <b>GetTempFileName</b>  instead.</div>
<div> </div>


</td>
</tr>
<tr>
<td>MMIO_PARSE</td>
<td>
Creates a fully qualified file name from the path specified in <i>szFilename</i>. The fully qualified name is copied to the buffer pointed to by <i>szFilename</i>.  The buffer must be large enough to hold at least 128 characters.

 If the function succeeds, the return value is <b>TRUE</b> (cast to <b>HMMIO</b>). Otherwise, the return value is <b>FALSE</b>. The file is not opened, and the function does not return a valid multimedia file I/O file handle, so do not attempt to close the file. If this flag is specified, all flags that open files are ignored.


<div class="alert"><b>Note</b>  Applications should call <b>GetFullPathName</b>  instead.</div>
<div> </div>


</td>
</tr>
<tr>
<td>MMIO_READ</td>
<td>Opens the file for reading only. This is the default if MMIO_WRITE and MMIO_READWRITE are not specified.</td>
</tr>
<tr>
<td>MMIO_READWRITE</td>
<td>Opens the file for reading and writing.</td>
</tr>
<tr>
<td>MMIO_WRITE</td>
<td>Opens the file for writing only.</td>
</tr>
</table>

## -remarks

If <i>lpmmioinfo</i> points to an <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure, initialize the members of the structure as follows. All unused members must be set to zero, including reserved members.

<ul>
<li>To request that a file be opened with an installed I/O procedure, set <b>fccIOProc</b> to the four-character code of the I/O procedure, and set <b>pIOProc</b> to <b>NULL</b>.</li>
<li>To request that a file be opened with an uninstalled I/O procedure, set <a href="/previous-versions/dd757098(v=vs.85)">IOProc</a> to point to the I/O procedure, and set <b>fccIOProc</b> to <b>NULL</b>.</li>
<li>To request that <b>mmioOpen</b> determine which I/O procedure to use to open the file based on the file name contained in <i>szFilename</i>, set <b>fccIOProc</b> and <b>pIOProc</b> to <b>NULL</b>. This is the default behavior if no <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure is specified.</li>
<li>To open a memory file using an internally allocated and managed buffer, set <b>pchBuffer</b> to <b>NULL</b>, <b>fccIOProc</b> to FOURCC_MEM, <b>cchBuffer</b> to the initial size of the buffer, and <b>adwInfo</b> to the incremental expansion size of the buffer. This memory file will automatically be expanded in increments of the number of bytes specified in <b>adwInfo</b> when necessary. Specify the MMIO_CREATE flag for the <i>dwOpenFlags</i> parameter to initially set the end of the file to be the beginning of the buffer.</li>
<li>To open a memory file using an application-supplied buffer, set <b>pchBuffer</b> to point to the memory buffer, <b>fccIOProc</b> to FOURCC_MEM, <b>cchBuffer</b> to the size of the buffer, and <b>adwInfo</b> to the incremental expansion size of the buffer. The expansion size in <b>adwInfo</b> should be nonzero only if <b>pchBuffer</b> is a pointer obtained by calling the <a href="/windows/win32/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> and <a href="/windows/win32/api/winbase/nf-winbase-globallock">GlobalLock</a> functions; in this case, the <a href="/windows/win32/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> function will be called to expand the buffer. In other words, if <b>pchBuffer</b> points to a local or global array or a block of memory in the local heap, <b>adwInfo</b> must be zero. Specify the MMIO_CREATE flag for the <i>dwOpenFlags</i> parameter to initially set the end of the file to be the beginning of the buffer. Otherwise, the entire block of memory is considered readable.</li>
<li>To use a currently open standard file handle (that is, a file handle that does not have the <b>HMMIO</b> type) with multimedia file I/O services, set <b>fccIOProc</b> to FOURCC_DOS, <b>pchBuffer</b> to <b>NULL</b>, and <b>adwInfo</b> to the standard file handle. Offsets within the file will be relative to the beginning of the file and are not related to the position in the standard file at the time <b>mmioOpen</b> is called; the initial multimedia file I/O offset will be the same as the offset in the standard file when <b>mmioOpen</b> is called. To close the multimedia file I/O file handle without closing the standard file handle, pass the MMIO_FHOPEN flag to <a href="/previous-versions/dd757316(v=vs.85)">mmioClose</a>.</li>
</ul>
You must call <a href="/previous-versions/dd757316(v=vs.85)">mmioClose</a> to close a file opened by using <b>mmioOpen</b>. Open files are not automatically closed when an application exits.




> [!NOTE]
> The mmiscapi.h header defines mmioOpen as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
