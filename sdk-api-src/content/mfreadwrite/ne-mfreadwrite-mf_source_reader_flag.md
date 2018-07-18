---
UID: NE:mfreadwrite.MF_SOURCE_READER_FLAG
title: MF_SOURCE_READER_FLAG
author: windows-sdk-content
description: Contains flags that indicate the status of the IMFSourceReader::ReadSample method.
old-location: mf\mf_source_reader_flag.htm
old-project: medfound
ms.assetid: 8981a682-3c0b-458b-910a-d1462ed73e64
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: MF_SOURCE_READERF_ALLEFFECTSREMOVED, MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED, MF_SOURCE_READERF_ENDOFSTREAM, MF_SOURCE_READERF_ERROR, MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED, MF_SOURCE_READERF_NEWSTREAM, MF_SOURCE_READERF_STREAMTICK, MF_SOURCE_READER_FLAG, MF_SOURCE_READER_FLAG enumeration [Media Foundation], mf.mf_source_reader_flag, mfreadwrite/MF_SOURCE_READERF_ALLEFFECTSREMOVED, mfreadwrite/MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED, mfreadwrite/MF_SOURCE_READERF_ENDOFSTREAM, mfreadwrite/MF_SOURCE_READERF_ERROR, mfreadwrite/MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED, mfreadwrite/MF_SOURCE_READERF_NEWSTREAM, mfreadwrite/MF_SOURCE_READERF_STREAMTICK, mfreadwrite/MF_SOURCE_READER_FLAG
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfreadwrite.h
api_name:
 - MF_SOURCE_READER_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MF_SOURCE_READER_FLAG enumeration


## -description


Contains flags that indicate the status of the <a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">IMFSourceReader::ReadSample</a> method.


## -enum-fields




### -field MF_SOURCE_READERF_ERROR

An error occurred. If you receive this flag, do not make any further calls to <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a> methods.


### -field MF_SOURCE_READERF_ENDOFSTREAM

The source reader reached the end of the stream.


### -field MF_SOURCE_READERF_NEWSTREAM

One or more new streams were created. Respond to this flag by doing at least one of the following:

<ul>
<li>Set the output types on the new streams.</li>
<li>Update the stream selection by selecting or deselecting streams.</li>
</ul>

### -field MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED

The <i>native format</i> has changed for one or more streams. The native format is the format delivered by the media source before any decoders are inserted.


### -field MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED

The current media has type changed for one or more streams. To get the current media type, call the <a href="https://msdn.microsoft.com/c0fe3b34-42ad-45e4-812d-679bbe01a200">IMFSourceReader::GetCurrentMediaType</a> method.


### -field MF_SOURCE_READERF_STREAMTICK

There is a gap in the stream. This flag corresponds to an <a href="https://msdn.microsoft.com/1a00fff1-c3ab-4965-a663-3c15bb48ea98">MEStreamTick</a> event from the media source.


### -field MF_SOURCE_READERF_ALLEFFECTSREMOVED

All transforms inserted by the application have been removed for a particular stream. This could be due to a dynamic format change from a source or decoder that prevents custom transforms from being used because they cannot handle the new media type.


## -see-also




<a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

