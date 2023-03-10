---
UID: NS:wmcodecdsp._TOC_ENTRY_DESCRIPTOR
title: TOC_ENTRY_DESCRIPTOR (wmcodecdsp.h)
description: The TOC_ENTRY_DESCRIPTOR structure holds descriptive information for an entry in a table of contents.
helpviewer_keywords: ["TOC_ENTRY_DESCRIPTOR","TOC_ENTRY_DESCRIPTOR structure [Media Foundation]","codecapi.toc_entry_descriptor","mf.toc_entry_descriptor","wmcodecdsp/TOC_ENTRY_DESCRIPTOR"]
old-location: mf\toc_entry_descriptor.htm
tech.root: mf
ms.assetid: 05e9bf59-5dd8-410f-8e42-25bfb555dd40
ms.date: 12/05/2018
ms.keywords: TOC_ENTRY_DESCRIPTOR, TOC_ENTRY_DESCRIPTOR structure [Media Foundation], codecapi.toc_entry_descriptor, mf.toc_entry_descriptor, wmcodecdsp/TOC_ENTRY_DESCRIPTOR
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TOC_ENTRY_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOC_ENTRY_DESCRIPTOR
 - wmcodecdsp/_TOC_ENTRY_DESCRIPTOR
 - TOC_ENTRY_DESCRIPTOR
 - wmcodecdsp/TOC_ENTRY_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcodecdsp.h
api_name:
 - TOC_ENTRY_DESCRIPTOR
---

# TOC_ENTRY_DESCRIPTOR structure


## -description

The <b>TOC_ENTRY_DESCRIPTOR</b> structure holds descriptive information for an entry in a table of contents. An entry in a table of contents describes a portion of a media file. For example, an entry might describe a ten-second chunk of video that  starts 90 seconds after the beginning of a video file.

## -struct-fields

### -field qwStartTime

The start time, in 100-nanosecond units, of the portion of a media file represented by an entry in a table of contents.

### -field qwEndTime

The end time, in 100-nanosecond units, of the portion of a media file represented by an entry in a table of contents.

### -field qwStartPacketOffset

Not used.

### -field qwEndPacketOffset

Not used.

### -field qwRepresentativeFrameTime

The presentation time, in 100-nanosecond units, of a frame that is a good representation of the entry. This frame could be used for a thumbnail image that represents the entry.

## -see-also

<a href="/windows/desktop/medfound/toc-parser-structures">Table of Contents Parser Structures</a>