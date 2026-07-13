---
UID: NE:objidl.tagSTREAM_SEEK
title: STREAM_SEEK (objidl.h)
description: The STREAM_SEEK enumeration values specify the origin from which to calculate the new seek-pointer location.
helpviewer_keywords: ["STREAM_SEEK","STREAM_SEEK enumeration [Structured Storage]","STREAM_SEEK_CUR","STREAM_SEEK_END","STREAM_SEEK_SET","_stg_stream_seek","objidl/STREAM_SEEK","objidl/STREAM_SEEK_CUR","objidl/STREAM_SEEK_END","objidl/STREAM_SEEK_SET","stg.stream_seek"]
old-location: stg\stream_seek.htm
tech.root: Stg
ms.assetid: f73a8f98-c004-40c7-b8d2-5b84d7aa2c31
ms.date: 12/05/2018
ms.keywords: STREAM_SEEK, STREAM_SEEK enumeration [Structured Storage], STREAM_SEEK_CUR, STREAM_SEEK_END, STREAM_SEEK_SET, _stg_stream_seek, objidl/STREAM_SEEK, objidl/STREAM_SEEK_CUR, objidl/STREAM_SEEK_END, objidl/STREAM_SEEK_SET, stg.stream_seek
req.header: objidl.h
req.include-header: 
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
req.typenames: STREAM_SEEK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTREAM_SEEK
 - objidl/tagSTREAM_SEEK
 - STREAM_SEEK
 - objidl/STREAM_SEEK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - STREAM_SEEK
---

# STREAM_SEEK enumeration


## -description

The 
<b>STREAM_SEEK</b> enumeration values specify the origin from which to calculate the new seek-pointer location. They are used for the <i>dworigin</i> parameter in the 
<a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">IStream::Seek</a> method. The new seek position is calculated using this value and the <i>dlibMove</i> parameter.

## -enum-fields

### -field STREAM_SEEK_SET:0

The new seek pointer is an offset relative to the beginning of the stream. In this case, the <i>dlibMove</i> parameter is the new seek position relative to the beginning of the stream.

### -field STREAM_SEEK_CUR:1

The new seek pointer is an offset relative to the current seek pointer location. In this case, the <i>dlibMove</i> parameter is the signed displacement from the current seek position.

### -field STREAM_SEEK_END:2

The new seek pointer is an offset relative to the end of the stream. In this case, the <i>dlibMove</i> parameter is the new seek position relative to the end of the stream.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">IStream::Seek</a>
