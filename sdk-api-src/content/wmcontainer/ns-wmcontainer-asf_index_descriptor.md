---
UID: NS:wmcontainer._ASF_INDEX_DESCRIPTOR
title: ASF_INDEX_DESCRIPTOR (wmcontainer.h)
description: Describes the indexing configuration for a stream and type of index.
helpviewer_keywords: ["2a540aef-068d-4465-b0ed-64aed828af01","ASF_INDEX_DESCRIPTOR","ASF_INDEX_DESCRIPTOR structure [Media Foundation]","mf.asf_index_descriptor","wmcontainer/ASF_INDEX_DESCRIPTOR"]
old-location: mf\asf_index_descriptor.htm
tech.root: mf
ms.assetid: 2a540aef-068d-4465-b0ed-64aed828af01
ms.date: 12/05/2018
ms.keywords: 2a540aef-068d-4465-b0ed-64aed828af01, ASF_INDEX_DESCRIPTOR, ASF_INDEX_DESCRIPTOR structure [Media Foundation], mf.asf_index_descriptor, wmcontainer/ASF_INDEX_DESCRIPTOR
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
req.typenames: ASF_INDEX_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ASF_INDEX_DESCRIPTOR
 - wmcontainer/_ASF_INDEX_DESCRIPTOR
 - ASF_INDEX_DESCRIPTOR
 - wmcontainer/ASF_INDEX_DESCRIPTOR
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
 - ASF_INDEX_DESCRIPTOR
---

# ASF_INDEX_DESCRIPTOR structure


## -description

Describes the indexing configuration for a stream and type of index.

## -struct-fields

### -field Identifier

<a href="/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier">ASF_INDEX_IDENTIFIER</a> structure that identifies the stream number and the type of index.

### -field cPerEntryBytes

Number of bytes used for each index entry. If the value is MFASFINDEXER_PER_ENTRY_BYTES_DYNAMIC, the index entries have variable size.

### -field szDescription

Optional text description of the index.

### -field dwInterval

Indexing interval. The units of this value depend on the index type. A value of MFASFINDEXER_NO_FIXED_INTERVAL indicates that there is no fixed indexing interval.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus">IMFASFIndexer::GetIndexStatus</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus">IMFASFIndexer::SetIndexStatus</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>