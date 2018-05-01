---
UID: NS:aviriff._avimetaindex
title: "_avimetaindex"
author: windows-driver-content
description: The base structure for an AVI 2.0 index ('indx' format).
old-location: dshow\avimetaindex.htm
old-project: DirectShow
ms.assetid: d27b2b14-55a1-4992-ad85-75244369accc
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: AVIMETAINDEX, AVIMETAINDEX structure [DirectShow], AVI_INDEX_IS_DATA, AVI_INDEX_OF_CHUNKS, AVI_INDEX_OF_INDEXES, _avimetaindex, aviriff/AVIMETAINDEX, dshow.avimetaindex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: aviriff.h
req.include-header: 
req.target-type: Windows
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
req.typenames: AVIMETAINDEX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	aviriff.h
api_name:
-	AVIMETAINDEX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _avimetaindex structure


## -description


The base structure for an AVI 2.0 index ('indx' format).


## -struct-fields




### -field fcc

A <b>FOURCC</b> code. The value is either  'indx' or '<i>nn</i>ix', where <i>nn</i> is the stream number.


### -field cb

The size of the structure, not including the initial 8 bytes.


### -field wLongsPerEntry

The size of each index entry, in 4-byte units.


### -field bIndexSubType

The index subtype. The meaning depends on the value of <b>bIndexType</b>.


### -field bIndexType

The index type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AVI_INDEX_OF_INDEXES"></a><a id="avi_index_of_indexes"></a><dl>
<dt><b>AVI_INDEX_OF_INDEXES</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Each index entry points to another index. Treat the <b>AVIMETAINDEX</b> structure as an <a href="https://msdn.microsoft.com/57c855ef-d4ea-4e11-a37b-941335ccf657">AVISUPERINDEX</a> structure. The value of <b>bIndexSubType</b> must be zero.

</td>
</tr>
<tr>
<td width="40%"><a id="AVI_INDEX_OF_CHUNKS"></a><a id="avi_index_of_chunks"></a><dl>
<dt><b>AVI_INDEX_OF_CHUNKS</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Each index entry points to a data chunk in the file. 

<ul>
<li>If <b>bIndexSubType</b> is 0,  treat the <b>AVIMETAINDEX</b> structure as an <a href="https://msdn.microsoft.com/b437b333-84a3-44d3-a4cc-0d07a331b010">AVISTDINDEX</a> structure. Each index entry is an <a href="https://msdn.microsoft.com/4e408858-b0cb-45dc-a299-a2e35aa6a000">AVISTDINDEX_ENTRY</a> structure.</li>
<li>If <b>bIndexSubType</b> is <b>AVI_INDEX_SUB_2FIELD</b>, the index is a field index chunk.<div class="alert"><b>Note</b>  DirectShow does not support field indexes.</div>
<div> </div>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="AVI_INDEX_IS_DATA"></a><a id="avi_index_is_data"></a><dl>
<dt><b>AVI_INDEX_IS_DATA</b></dt>
<dt>0x80</dt>
</dl>
</td>
<td width="60%">
The <b>adwIndex</b> array contains a table of data, not a list of index entries.

</td>
</tr>
</table>
 


### -field nEntriesInUse

The number of valid entries in the <b>adwIndex</b> array.


### -field dwChunkId

A <b>FOURCC</b> that identifies the object that is indexed. If the indexed object is a stream, this member has the same meaning as the <b>dwChunkId</b>  member of the <a href="https://msdn.microsoft.com/c36d5759-710e-4abe-85dc-13462013bb9f">AVIOLDINDEX</a> structure.


### -field dwReserved

The meaning of this member depends on the index type.


### -field adwIndex

An array of index entries. The format of this data depends on the index type.


## -remarks



For more information, see the <i>OpenDML AVI File Format Extensions</i>, published by the OpenDML AVI M-JPEG File Format Subcommittee. (This resource may not be available in some languages 

and countries.)




## -see-also




<a href="https://msdn.microsoft.com/2d8cf5be-1252-4b58-89b1-f5c53ea17d0e">AVI RIFF File Reference</a>



<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

