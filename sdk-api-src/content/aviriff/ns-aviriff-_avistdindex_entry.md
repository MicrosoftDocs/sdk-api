---
UID: NS:aviriff._avistdindex_entry
title: "_avistdindex_entry"
author: windows-sdk-content
description: Contains one index entry for an AVI 2.0 standard index.
old-location: dshow\avistdindex_entry.htm
tech.root: DirectShow
ms.assetid: 4e408858-b0cb-45dc-a299-a2e35aa6a000
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AVISTDINDEX_ENTRY, AVISTDINDEX_ENTRY structure [DirectShow], _avistdindex_entry, aviriff/AVISTDINDEX_ENTRY, dshow.avistdindex_entry
ms.prod: windows
ms.technology: windows-sdk
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
 - AVISTDINDEX_ENTRY
product: Windows
targetos: Windows
req.typenames: AVISTDINDEX_ENTRY
req.redist: 
---

# _avistdindex_entry structure


## -description


Contains one index entry for an AVI 2.0 standard index. This structure is contained in the <a href="https://msdn.microsoft.com/b437b333-84a3-44d3-a4cc-0d07a331b010">AVISTDINDEX</a> structure.


## -struct-fields




### -field dwOffset

The offset, in bytes, to the start of the data. The offset is relative to the value of the <b>qwBaseOffset</b> member of the <a href="https://msdn.microsoft.com/b437b333-84a3-44d3-a4cc-0d07a331b010">AVISTDINDEX</a>. The value is the offset of the actual audio/video data in the chunk, not the offset of the start of the chunk.


### -field dwSize

The lower 31 bits contain the size of the data. The high bit is set to 1 if the frame is delta frame, or zero otherwise.


## -remarks



For more information, see the <i>OpenDML AVI File Format Extensions</i>, published by the OpenDML AVI M-JPEG File Format Subcommittee. (This resource may not be available in some languages 

and countries.)




## -see-also




<a href="https://msdn.microsoft.com/2d8cf5be-1252-4b58-89b1-f5c53ea17d0e">AVI RIFF File Reference</a>



<a href="https://msdn.microsoft.com/b437b333-84a3-44d3-a4cc-0d07a331b010">AVISTDINDEX</a>



<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

