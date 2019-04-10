---
UID: NS:mpegtype.tagAM_MPEGSYSTEMTYPE
title: AM_MPEGSYSTEMTYPE (mpegtype.h)
author: windows-sdk-content
description: The AM_MPEGSYSTEMTYPE structure defines the format block for an MPEG-1 system stream.
old-location: dshow\am_mpegsystemtype.htm
tech.root: DirectShow
ms.assetid: 218bf0c3-e618-4dcc-8618-34cd1fb5c0a8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AM_MPEGSYSTEMTYPE, AM_MPEGSYSTEMTYPE structure [DirectShow], dshow.am_mpegsystemtype, mpegtype/AM_MPEGSYSTEMTYPE
ms.topic: struct
req.header: mpegtype.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mpegtype.h
api_name:
 - AM_MPEGSYSTEMTYPE
product: Windows
targetos: Windows
req.typenames: AM_MPEGSYSTEMTYPE
req.redist: 
---

# AM_MPEGSYSTEMTYPE structure


## -description


The <b>AM_MPEGSYSTEMTYPE</b> structure defines the format block for an MPEG-1 system stream. This structure is used when the <b>formattype</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Dd373477(v=VS.85).aspx">AM_MEDIA_TYPE</a> structure is FORMAT_MPEG1System.
        


## -struct-fields




### -field dwBitRate

Bits per second.


### -field cStreams

Number of streams.


### -field Streams

List <a href="https://msdn.microsoft.com/en-us/library/Dd373480(v=VS.85).aspx">AM_MPEGSTREAMTYPE</a> structures that describe the elementary streams. The number of elements in the list is given by the <b>cStream</b> member. The size of each <b>AM_MPEGSTREAMTYPE</b> structure is variable. Use the <b>AM_MPEGSTREAMTYPE_ELEMENTLENGTH</b> macro to calculate the size of each structure.


## -remarks



The <b>Streams</b> member contains a list of <a href="https://msdn.microsoft.com/en-us/library/Dd373480(v=VS.85).aspx">AM_MPEGSTREAMTYPE</a> structures. The size of each <b>AM_MPEGSTREAMTYPE</b> structure is aligned to an 8-byte boundary. Given a pointer to an <b>AM_MPEGSTREAMTYPE</b> structure in list, use the <b>AM_MPEGSTREAMTYPE_NEXT</b> macro to get a pointer to the next structure.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8">MEPG-1 Media Types</a>
 

 

