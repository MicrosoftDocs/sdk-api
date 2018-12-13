---
UID: NS:aviriff._avistdindex
title: AVISTDINDEX
author: windows-sdk-content
description: Contains an AVI 2.0 standard index.
old-location: dshow\avistdindex.htm
tech.root: DirectShow
ms.assetid: b437b333-84a3-44d3-a4cc-0d07a331b010
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AVISTDINDEX, AVISTDINDEX structure [DirectShow], PAVISTDINDEX, PAVISTDINDEX structure pointer [DirectShow], aviriff/AVISTDINDEX, aviriff/PAVISTDINDEX, dshow.avistdindex
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - aviriff.h
api_name:
 - AVISTDINDEX
product: Windows
targetos: Windows
req.typenames: AVISTDINDEX
req.redist: 
---

# AVISTDINDEX structure


## -description


Contains an AVI 2.0 standard index.


## -struct-fields




### -field fcc

A <b>FOURCC</b> code. The value is either  'indx' or '<i>nn</i>ix', where <i>nn</i> is the stream number.


### -field cb

The size of the structure, not including the initial 8 bytes.


### -field wLongsPerEntry

The size of each index entry, in 4-byte units. The value must be 2.


### -field bIndexSubType

The index subtype. The value must be zero.


### -field bIndexType

The index type. The value must be <b>AVI_INDEX_OF_CHUNKS</b>.


### -field nEntriesInUse

The number of valid entries in the <b>adwIndex</b> array.


### -field dwChunkId

A <b>FOURCC</b> that identifies the object that is indexed. This member has the same meaning as the <b>dwChunkId</b>  member of the <a href="https://msdn.microsoft.com/c36d5759-710e-4abe-85dc-13462013bb9f">AVIOLDINDEX</a> structure.


### -field qwBaseOffset

The base offset for the index entries. For each index entry, <b>qwBaseOffset</b> + <b>AVISTDINDEX_ENTRY.dwOffset</b> gives the offset from the start of the file to the data.


### -field dwReserved_3

Reserved. Set to zero.


### -field aIndex

An array of <a href="https://msdn.microsoft.com/4e408858-b0cb-45dc-a299-a2e35aa6a000">AVISTDINDEX_ENTRY</a> structures. The number of elements in the array is calculated from the value of <b>cb</b>.


## -remarks



For more information, see the <i>OpenDML AVI File Format Extensions</i>, published by the OpenDML AVI M-JPEG File Format Subcommittee. (This resource may not be available in some languages 

and countries.)




## -see-also




<a href="https://msdn.microsoft.com/2d8cf5be-1252-4b58-89b1-f5c53ea17d0e">AVI RIFF File Reference</a>



<a href="https://msdn.microsoft.com/d27b2b14-55a1-4992-ad85-75244369accc">AVIMETAINDEX</a>



<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

