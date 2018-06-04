---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

