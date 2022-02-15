---
UID: NE:wmcontainer.MFASF_INDEXERFLAGS
title: MFASF_INDEXER_FLAGS (wmcontainer.h)
description: Defines the ASF indexer options.
helpviewer_keywords: ["MFASF_INDEXER_FLAGS","MFASF_INDEXER_FLAGS enumeration [Media Foundation]","MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK","MFASF_INDEXER_WRITE_FOR_LIVEREAD","MFASF_INDEXER_WRITE_NEW_INDEX","e5794835-218d-4759-bf3e-a573b24424c3","enumeration [Media Foundation]","mf.mfasf_indexer_flags","wmcontainer/MFASF_INDEXER_FLAGS","wmcontainer/MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK","wmcontainer/MFASF_INDEXER_WRITE_FOR_LIVEREAD","wmcontainer/MFASF_INDEXER_WRITE_NEW_INDEX"]
old-location: mf\mfasf_indexer_flags.htm
tech.root: mf
ms.assetid: e5794835-218d-4759-bf3e-a573b24424c3
ms.date: 12/05/2018
ms.keywords: MFASF_INDEXER_FLAGS, MFASF_INDEXER_FLAGS enumeration [Media Foundation], MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK, MFASF_INDEXER_WRITE_FOR_LIVEREAD, MFASF_INDEXER_WRITE_NEW_INDEX, e5794835-218d-4759-bf3e-a573b24424c3, enumeration [Media Foundation], mf.mfasf_indexer_flags, wmcontainer/MFASF_INDEXER_FLAGS, wmcontainer/MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK, wmcontainer/MFASF_INDEXER_WRITE_FOR_LIVEREAD, wmcontainer/MFASF_INDEXER_WRITE_NEW_INDEX
req.header: wmcontainer.h
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
req.typenames: MFASF_INDEXER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFASF_INDEXERFLAGS
 - wmcontainer/MFASF_INDEXERFLAGS
 - MFASF_INDEXER_FLAGS
 - wmcontainer/MFASF_INDEXER_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcontainer.h
api_name:
 - MFASF_INDEXER_FLAGS
---

# MFASF_INDEXER_FLAGS enumeration


## -description

Defines the ASF indexer options.

## -enum-fields

### -field MFASF_INDEXER_WRITE_NEW_INDEX:0x1

The indexer creates a new index object.

### -field MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK:0x2

The indexer returns values for reverse playback.

### -field MFASF_INDEXER_WRITE_FOR_LIVEREAD:0x4

The indexer creates an index object for a live ASF stream.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
