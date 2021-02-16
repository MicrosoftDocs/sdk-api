---
UID: NS:wmcontainer._ASF_INDEX_IDENTIFIER
title: ASF_INDEX_IDENTIFIER (wmcontainer.h)
description: Specifies an index for the ASF indexer object.
helpviewer_keywords: ["8103a62e-6d1a-4dcd-af91-cedb30523004","ASF_INDEX_IDENTIFIER","ASF_INDEX_IDENTIFIER structure [Media Foundation]","mf.asf_index_identifier","wmcontainer/ASF_INDEX_IDENTIFIER"]
old-location: mf\asf_index_identifier.htm
tech.root: mf
ms.assetid: 8103a62e-6d1a-4dcd-af91-cedb30523004
ms.date: 12/05/2018
ms.keywords: 8103a62e-6d1a-4dcd-af91-cedb30523004, ASF_INDEX_IDENTIFIER, ASF_INDEX_IDENTIFIER structure [Media Foundation], mf.asf_index_identifier, wmcontainer/ASF_INDEX_IDENTIFIER
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
req.typenames: ASF_INDEX_IDENTIFIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ASF_INDEX_IDENTIFIER
 - wmcontainer/_ASF_INDEX_IDENTIFIER
 - ASF_INDEX_IDENTIFIER
 - wmcontainer/ASF_INDEX_IDENTIFIER
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
 - ASF_INDEX_IDENTIFIER
---

# ASF_INDEX_IDENTIFIER structure


## -description

Specifies an index for the ASF indexer object.

## -struct-fields

### -field guidIndexType

The type of index. Currently this value must be GUID_NULL, which specifies time-based indexing.

### -field wStreamNumber

The stream number to which this structure applies.

## -remarks

The index object of an ASF file can contain a number of distinct indexes. Each index is identified by the type of index and the stream number. No ASF index object can contain more than one index for a particular combination of stream number and index type.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus">IMFASFIndexer::GetIndexStatus</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus">IMFASFIndexer::SetIndexStatus</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>