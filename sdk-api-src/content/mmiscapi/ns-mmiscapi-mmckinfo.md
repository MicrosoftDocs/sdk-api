---
UID: NS:mmiscapi._MMCKINFO
title: MMCKINFO (mmiscapi.h)
description: The MMCKINFO structure contains information about a chunk in a RIFF file.
helpviewer_keywords: ["*LPMMCKINFO","*NPMMCKINFO","*PMMCKINFO","MMCKINFO","MMCKINFO structure [Windows Multimedia]","MMIO_DIRTY","_MMCKINFO","_win32_MMCKINFO_str","mmiscapi/MMCKINFO","multimedia.mmckinfo"]
old-location: multimedia\mmckinfo.htm
tech.root: Multimedia
ms.assetid: 5ea2569f-a15b-47f4-8d86-0bc005019984
ms.date: 12/05/2018
ms.keywords: '*LPMMCKINFO, *NPMMCKINFO, *PMMCKINFO, MMCKINFO, MMCKINFO structure [Windows Multimedia], MMIO_DIRTY, _MMCKINFO, _win32_MMCKINFO_str, mmiscapi/MMCKINFO, multimedia.mmckinfo'
req.header: mmiscapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MMCKINFO, *PMMCKINFO, *NPMMCKINFO, *LPMMCKINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMCKINFO
 - mmiscapi/_MMCKINFO
 - PMMCKINFO
 - mmiscapi/PMMCKINFO
 - MMCKINFO
 - mmiscapi/MMCKINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmiscapi.h
api_name:
 - MMCKINFO
---

# MMCKINFO structure


## -description

The <b>MMCKINFO</b> structure contains information about a chunk in a RIFF file.

## -struct-fields

### -field ckid

Chunk identifier.

### -field cksize

Size, in bytes, of the data member of the chunk. The size of the data member does not include the 4-byte chunk identifier, the 4-byte chunk size, or the optional pad byte at the end of the data member.

### -field fccType

Form type for "RIFF" chunks or the list type for "LIST" chunks.

### -field dwDataOffset

File offset of the beginning of the chunk's data member, relative to the beginning of the file.

### -field dwFlags

Flags specifying additional information about the chunk. It can be zero or the following flag:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MMIO_DIRTY"></a><a id="mmio_dirty"></a><dl>
<dt><b>MMIO_DIRTY</b></dt>
</dl>
</td>
<td width="60%">
The length of the chunk might have changed and should be updated by the <a href="/previous-versions/dd757315(v=vs.85)">mmioAscend</a> function. This flag is set when a chunk is created by using the <a href="/previous-versions/dd757317(v=vs.85)">mmioCreateChunk</a> function.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/dd757315(v=vs.85)">mmioAscend</a>



<a href="/previous-versions/dd757317(v=vs.85)">mmioCreateChunk</a>