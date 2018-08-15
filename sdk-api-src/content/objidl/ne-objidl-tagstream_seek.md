---
UID: NE:objidl.tagSTREAM_SEEK
title: tagSTREAM_SEEK
author: windows-sdk-content
description: The STREAM_SEEK enumeration values specify the origin from which to calculate the new seek-pointer location.
old-location: stg\stream_seek.htm
old-project: stg
ms.assetid: f73a8f98-c004-40c7-b8d2-5b84d7aa2c31
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: STREAM_SEEK, STREAM_SEEK enumeration [Structured Storage], STREAM_SEEK_CUR, STREAM_SEEK_END, STREAM_SEEK_SET, _stg_stream_seek, objidl/STREAM_SEEK, objidl/STREAM_SEEK_CUR, objidl/STREAM_SEEK_END, objidl/STREAM_SEEK_SET, stg.stream_seek, tagSTREAM_SEEK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STREAM_SEEK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - STREAM_SEEK
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: ADAM
---

# tagSTREAM_SEEK enumeration


## -description


The 
<b>STREAM_SEEK</b> enumeration values specify the origin from which to calculate the new seek-pointer location. They are used for the <i>dworigin</i> parameter in the 
<a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">IStream::Seek</a> method. The new seek position is calculated using this value and the <i>dlibMove</i> parameter.


## -enum-fields




### -field STREAM_SEEK_SET

The new seek pointer is an offset relative to the beginning of the stream. In this case, the <i>dlibMove</i> parameter is the new seek position relative to the beginning of the stream.


### -field STREAM_SEEK_CUR

The new seek pointer is an offset relative to the current seek pointer location. In this case, the <i>dlibMove</i> parameter is the signed displacement from the current seek position.


### -field STREAM_SEEK_END

The new seek pointer is an offset relative to the end of the stream. In this case, the <i>dlibMove</i> parameter is the new seek position relative to the end of the stream.


## -see-also




<a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">IStream::Seek</a>
 

 

