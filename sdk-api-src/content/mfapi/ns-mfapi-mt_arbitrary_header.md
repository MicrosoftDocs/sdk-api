---
UID: NS:mfapi._MT_ARBITRARY_HEADER
title: MT_ARBITRARY_HEADER (mfapi.h)
description: Contains format data for a binary stream in an Advanced Streaming Format (ASF) file.
helpviewer_keywords: ["MT_ARBITRARY_HEADER","MT_ARBITRARY_HEADER structure [Media Foundation]","mf.mt_arbitrary_header","mfapi/MT_ARBITRARY_HEADER"]
old-location: mf\mt_arbitrary_header.htm
tech.root: mf
ms.assetid: efe2ceb7-32f5-4a43-b4d9-807fe66d6edb
ms.date: 12/05/2018
ms.keywords: MT_ARBITRARY_HEADER, MT_ARBITRARY_HEADER structure [Media Foundation], mf.mt_arbitrary_header, mfapi/MT_ARBITRARY_HEADER
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MT_ARBITRARY_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MT_ARBITRARY_HEADER
 - mfapi/_MT_ARBITRARY_HEADER
 - MT_ARBITRARY_HEADER
 - mfapi/MT_ARBITRARY_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MT_ARBITRARY_HEADER
---

# MT_ARBITRARY_HEADER structure


## -description

Contains format data for a binary stream in an Advanced Streaming Format (ASF) file.

## -struct-fields

### -field majortype

Major media type. This value is the GUID stored in the Major Media Type field of the Type-Specific Data field of the ASF file. It might not match the major type GUID from the Media Foundation media type.

### -field subtype

Media subtype.

### -field bFixedSizeSamples

If <b>TRUE</b>, samples have a fixed size in bytes.
          Otherwise, samples have variable size.

### -field bTemporalCompression

If <b>TRUE</b>, the data in this stream uses temporal compression. Otherwise, samples are independent of each other.

### -field lSampleSize

If <b>bFixedSizeSamples</b> is <b>TRUE</b>, this member specifies the sample size in bytes. Otherwise, the value is ignored and should be 0.

### -field formattype

Format type GUID. This GUID identifies the structure of the additional format data, which is stored in the 
          <a href="/windows/desktop/medfound/mf-mt-arbitrary-format">MF_MT_ARBITRARY_FORMAT</a> attribute of the media type. If no additional format data is present, <b>formattype</b> equals GUID_NULL.

## -remarks

This structure is used with the <a href="/windows/desktop/medfound/mf-mt-arbitrary-header">MF_MT_ARBITRARY_HEADER</a> media type attribute.

This structure corresponds to the first 60 bytes of the Type-Specific Data field of the Stream Properties Object, in files where the stream type is ASF_Binary_Media. For more information, see the ASF specification.

The Format Data field of the Type-Specific Data field is contained in the <a href="/windows/desktop/medfound/mf-mt-arbitrary-format">MF_MT_ARBITRARY_FORMAT</a> attribute of the media type.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>