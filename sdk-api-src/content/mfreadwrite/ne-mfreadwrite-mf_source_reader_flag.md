---
UID: NE:mfreadwrite.MF_SOURCE_READER_FLAG
title: MF_SOURCE_READER_FLAG (mfreadwrite.h)
description: Contains flags that indicate the status of the IMFSourceReader::ReadSample method.
helpviewer_keywords: ["MF_SOURCE_READERF_ALLEFFECTSREMOVED","MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED","MF_SOURCE_READERF_ENDOFSTREAM","MF_SOURCE_READERF_ERROR","MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED","MF_SOURCE_READERF_NEWSTREAM","MF_SOURCE_READERF_STREAMTICK","MF_SOURCE_READER_FLAG","MF_SOURCE_READER_FLAG enumeration [Media Foundation]","mf.mf_source_reader_flag","mfreadwrite/MF_SOURCE_READERF_ALLEFFECTSREMOVED","mfreadwrite/MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED","mfreadwrite/MF_SOURCE_READERF_ENDOFSTREAM","mfreadwrite/MF_SOURCE_READERF_ERROR","mfreadwrite/MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED","mfreadwrite/MF_SOURCE_READERF_NEWSTREAM","mfreadwrite/MF_SOURCE_READERF_STREAMTICK","mfreadwrite/MF_SOURCE_READER_FLAG"]
old-location: mf\mf_source_reader_flag.htm
tech.root: mf
ms.assetid: 8981a682-3c0b-458b-910a-d1462ed73e64
ms.date: 12/05/2018
ms.keywords: MF_SOURCE_READERF_ALLEFFECTSREMOVED, MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED, MF_SOURCE_READERF_ENDOFSTREAM, MF_SOURCE_READERF_ERROR, MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED, MF_SOURCE_READERF_NEWSTREAM, MF_SOURCE_READERF_STREAMTICK, MF_SOURCE_READER_FLAG, MF_SOURCE_READER_FLAG enumeration [Media Foundation], mf.mf_source_reader_flag, mfreadwrite/MF_SOURCE_READERF_ALLEFFECTSREMOVED, mfreadwrite/MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED, mfreadwrite/MF_SOURCE_READERF_ENDOFSTREAM, mfreadwrite/MF_SOURCE_READERF_ERROR, mfreadwrite/MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED, mfreadwrite/MF_SOURCE_READERF_NEWSTREAM, mfreadwrite/MF_SOURCE_READERF_STREAMTICK, mfreadwrite/MF_SOURCE_READER_FLAG
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: MF_SOURCE_READER_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_SOURCE_READER_FLAG
 - mfreadwrite/MF_SOURCE_READER_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfreadwrite.h
api_name:
 - MF_SOURCE_READER_FLAG
---

# MF_SOURCE_READER_FLAG enumeration


## -description

Contains flags that indicate the status of the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample">IMFSourceReader::ReadSample</a> method.

## -enum-fields

### -field MF_SOURCE_READERF_ERROR:0x1

An error occurred. If you receive this flag, do not make any further calls to <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a> methods.

### -field MF_SOURCE_READERF_ENDOFSTREAM:0x2

The source reader reached the end of the stream.

### -field MF_SOURCE_READERF_NEWSTREAM:0x4

One or more new streams were created. Respond to this flag by doing at least one of the following:

<ul>
<li>Set the output types on the new streams.</li>
<li>Update the stream selection by selecting or deselecting streams.</li>
</ul>

### -field MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED:0x10

The <i>native format</i> has changed for one or more streams. The native format is the format delivered by the media source before any decoders are inserted.

### -field MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED:0x20

The current media has type changed for one or more streams. To get the current media type, call the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype">IMFSourceReader::GetCurrentMediaType</a> method.

### -field MF_SOURCE_READERF_STREAMTICK:0x100

There is a gap in the stream. This flag corresponds to an <a href="/windows/desktop/medfound/mestreamtick">MEStreamTick</a> event from the media source.

### -field MF_SOURCE_READERF_ALLEFFECTSREMOVED:0x200

All transforms inserted by the application have been removed for a particular stream. This could be due to a dynamic format change from a source or decoder that prevents custom transforms from being used because they cannot handle the new media type.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
