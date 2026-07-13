---
UID: NF:vfw.AVIFileOpenA
title: AVIFileOpenA function (vfw.h)
description: The AVIFileOpen function opens an AVI file and returns the address of a file interface used to access it. (AVIFileOpenA)
helpviewer_keywords: ["AVIFileOpenA", "vfw/AVIFileOpenA"]
old-location: multimedia\avifileopen.htm
tech.root: Multimedia
ms.assetid: a5d7b278-7c80-42a3-94a4-5c012ad9a9fd
ms.date: 12/05/2018
ms.keywords: AVIFileOpen, AVIFileOpen function [Windows Multimedia], AVIFileOpenA, AVIFileOpenW, _win32_AVIFileOpen, multimedia.avifileopen, vfw/AVIFileOpen, vfw/AVIFileOpenA, vfw/AVIFileOpenW
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AVIFileOpenW (Unicode) and AVIFileOpenA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVIFileOpenA
 - vfw/AVIFileOpenA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIFileOpen
 - AVIFileOpenA
 - AVIFileOpenW
---

# AVIFileOpenA function


## -description

The <b>AVIFileOpen</b> function opens an AVI file and returns the address of a file interface used to access it. The AVIFile library maintains a count of the number of times a file is opened, but not the number of times it was released. Use the <a href="/windows/desktop/api/vfw/nf-vfw-avifilerelease">AVIFileRelease</a> function to release the file and decrement the count.

## -parameters

### -param ppfile

Pointer to a buffer that receives the new <a href="/windows/desktop/api/vfw/nn-vfw-iavifile">IAVIFile</a> interface pointer.

### -param szFile

Null-terminated string containing the name of the file to open.

### -param uMode

Access mode to use when opening the file. The default access mode is OF_READ. The following access modes can be specified with <b>AVIFileOpen</b>.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>OF_CREATE</td>
<td>Creates a new file. If the file already exists, it is truncated to zero length.</td>
</tr>
<tr>
<td>OF_PARSE</td>
<td>Skips time-consuming operations, such as building an index. Set this flag if you want the function to return as quickly as possible—for example, if you are going to query the file properties but not read the file.</td>
</tr>
<tr>
<td>OF_READ</td>
<td>Opens the file for reading.</td>
</tr>
<tr>
<td>OF_READWRITE</td>
<td>Opens the file for reading and writing.</td>
</tr>
<tr>
<td>OF_SHARE_DENY_NONE</td>
<td>Opens the file nonexclusively. Other processes can open the file with read or write access. <b>AVIFileOpen</b> fails if another process has opened the file in compatibility mode.</td>
</tr>
<tr>
<td>OF_SHARE_DENY_READ</td>
<td>Opens the file nonexclusively. Other processes can open the file with write access. <b>AVIFileOpen</b> fails if another process has opened the file in compatibility mode or has read access to it.</td>
</tr>
<tr>
<td>OF_SHARE_DENY_WRITE</td>
<td>Opens the file nonexclusively. Other processes can open the file with read access. <b>AVIFileOpen</b> fails if another process has opened the file in compatibility mode or has write access to it.</td>
</tr>
<tr>
<td>OF_SHARE_EXCLUSIVE</td>
<td>Opens the file and denies other processes any access to it. <b>AVIFileOpen</b> fails if any other process has opened the file.</td>
</tr>
<tr>
<td>OF_WRITE</td>
<td>Opens the file for writing.</td>
</tr>
</table>

### -param lpHandler

Pointer to a class identifier of the standard or custom handler you want to use. If the value is <b>NULL</b>, the system chooses a handler from the registry based on the file extension or the RIFF type specified in the file.

## -returns

Returns zero if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_BADFORMAT</b></dt>
</dl>
</td>
<td width="60%">
The file couldn't be read, indicating a corrupt file or an unrecognized format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The file could not be opened because of insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_FILEREAD</b></dt>
</dl>
</td>
<td width="60%">
A disk error occurred while reading the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_FILEOPEN</b></dt>
</dl>
</td>
<td width="60%">
A disk error occurred while opening the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
According to the registry, the type of file specified in <b>AVIFileOpen</b> does not have a handler to process it.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/api/vfw/nf-vfw-avifilerelease">AVIFileRelease</a>

## -remarks

> [!NOTE]
> The vfw.h header defines AVIFileOpen as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
