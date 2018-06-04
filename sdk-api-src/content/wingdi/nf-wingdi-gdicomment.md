---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GdiComment function


## -description


The <b>GdiComment</b> function copies a comment from a buffer into a specified enhanced-format metafile.


## -parameters




### -param hdc [in]

A handle to an enhanced-metafile device context.


### -param nSize

TBD


### -param lpData [in]

A pointer to the buffer that contains the comment.


#### - cbSize [in]

The length of the comment buffer, in bytes.


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
<td>The GDICOMMENT_WINDOWS_METAFILE public comment contains a Windows-format metafile that is equivalent to an enhanced-format metafile. This comment is written only by the <a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a> function. The comment record, if given, follows the <a href="https://msdn.microsoft.com/8e5f9a51-a995-48be-b936-1766fccb603a">ENHMETAHEADER</a> metafile record. The comment has the following form:</td>
</tr>
</table>
 

<pre class="syntax" xml:space="preserve"><code>
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
</code></pre>
<table>
<tr>
<td>GDICOMMENT_BEGINGROUP</td>
<td>The GDICOMMENT_BEGINGROUP public comment identifies the beginning of a group of drawing records. It identifies an object within an enhanced metafile. The comment has the following form:</td>
</tr>
</table>
 

<pre class="syntax" xml:space="preserve"><code>
DWORD   ident;         // This contains GDICOMMENT_IDENTIFIER.  
DWORD   iComment;      // This contains GDICOMMENT_BEGINGROUP.  
RECTL   rclOutput;     // This is the bounding rectangle for the  
                       // object in logical coordinates.  
DWORD   nDescription;  // This is the number of characters in the  
                       // optional Unicode description string that  
                       // follows. This is zero if there is no  
                       // description string.  
</code></pre>
<table>
<tr>
<td>GDICOMMENT_ENDGROUP</td>
<td>The GDICOMMENT_ENDGROUP public comment identifies the end of a group of drawing records. The GDICOMMENT_BEGINGROUP comment and the GDICOMMENT_ENDGROUP comment must be included in a pair and may be nested. The comment has the following form:</td>
</tr>
</table>
 

<pre class="syntax" xml:space="preserve"><code>
DWORD   ident;       // This contains GDICOMMENT_IDENTIFIER.  
DWORD   iComment;    // This contains GDICOMMENT_ENDGROUP.  
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/647f83ca-dca3-44af-a594-5f9ba2bd7607">CreateEnhMetaFile</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a>
 

 

