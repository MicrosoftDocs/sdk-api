---
UID: NF:wingdi.GdiComment
title: GdiComment function (wingdi.h)
description: The GdiComment function copies a comment from a buffer into a specified enhanced-format metafile.
helpviewer_keywords: ["GdiComment","GdiComment function [Windows GDI]","_win32_GdiComment","gdi.gdicomment","wingdi/GdiComment"]
old-location: gdi\gdicomment.htm
tech.root: gdi
ms.assetid: 80ed11fc-89f8-47ab-8b3b-c817733bd385
ms.date: 12/05/2018
ms.keywords: GdiComment, GdiComment function [Windows GDI], _win32_GdiComment, gdi.gdicomment, wingdi/GdiComment
req.header: wingdi.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GdiComment
 - wingdi/GdiComment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GdiComment
---

# GdiComment function


## -description

The <b>GdiComment</b> function copies a comment from a buffer into a specified enhanced-format metafile.

## -parameters

### -param hdc [in]

A handle to an enhanced-metafile device context.

### -param nSize [in]

The length of the comment buffer, in bytes.

### -param lpData [in]

A pointer to the buffer that contains the comment.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

A comment can include any kind of private information, for example, the source of a picture and the date it was created. A comment should begin with an application signature, followed by the data.

Comments should not contain application-specific or position-specific data. Position-specific data specifies the location of a record, and it should not be included because one metafile may be embedded within another metafile.

A public comment is a comment that begins with the comment signature identifier GDICOMMENT_IDENTIFIER. The following public comments are defined.

<table>
<tr>
<td>GDICOMMENT_WINDOWS_METAFILE</td>
<td>The GDICOMMENT_WINDOWS_METAFILE public comment contains a Windows-format metafile that is equivalent to an enhanced-format metafile. This comment is written only by the <a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a> function. The comment record, if given, follows the <a href="/windows/desktop/api/wingdi/ns-wingdi-enhmetaheader">ENHMETAHEADER</a> metafile record. The comment has the following form:</td>
</tr>
</table>
 


``` syntax

DWORD ident;         // This contains GDICOMMENT_IDENTIFIER.  
DWORD iComment;      // This contains GDICOMMENT_WINDOWS_METAFILE.  
DWORD nVersion;      // This contains the version number of the  
                     // Windows-format metafile.  
DWORD nChecksum;     // This is the additive DWORD checksum for  
                     // the enhanced metafile.  The checksum  
                     // for the enhanced metafile data including  
                     // this comment record must be zero.  
                     // Otherwise, the enhanced metafile has been  
                     //  modified and the Windows-format  
                     // metafile is no longer valid.  
DWORD fFlags;        // This must be zero.  
DWORD cbWinMetaFile; // This is the size, in bytes. of the  
                     // Windows-format metafile data that follows.  

```

<table>
<tr>
<td>GDICOMMENT_BEGINGROUP</td>
<td>The GDICOMMENT_BEGINGROUP public comment identifies the beginning of a group of drawing records. It identifies an object within an enhanced metafile. The comment has the following form:</td>
</tr>
</table>
 


``` syntax

DWORD   ident;         // This contains GDICOMMENT_IDENTIFIER.  
DWORD   iComment;      // This contains GDICOMMENT_BEGINGROUP.  
RECTL   rclOutput;     // This is the bounding rectangle for the  
                       // object in logical coordinates.  
DWORD   nDescription;  // This is the number of characters in the  
                       // optional Unicode description string that  
                       // follows. This is zero if there is no  
                       // description string.  

```

<table>
<tr>
<td>GDICOMMENT_ENDGROUP</td>
<td>The GDICOMMENT_ENDGROUP public comment identifies the end of a group of drawing records. The GDICOMMENT_BEGINGROUP comment and the GDICOMMENT_ENDGROUP comment must be included in a pair and may be nested. The comment has the following form:</td>
</tr>
</table>
 


``` syntax

DWORD   ident;       // This contains GDICOMMENT_IDENTIFIER.  
DWORD   iComment;    // This contains GDICOMMENT_ENDGROUP.  

```


## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createenhmetafilea">CreateEnhMetaFile</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a>
