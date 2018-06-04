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

# tagAM_MPEGSTREAMTYPE structure


## -description



          
          The <b>AM_MPEGSTREAMTYPE</b> structure defines the media type for an MPEG-1 program stream.
        


## -struct-fields




### -field dwStreamId

 


### -field dwReserved

Reserved.


### -field mt


<a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure describing the type for the substeam. The <b>pbFormat</b> member of this structure must <b>NULL</b>. The format data normally conveyed in <b>pbFormat</b> is stored in the <b>bFormat</b> member.


### -field bFormat

Format data. The size of this array, in bytes, is given in the <b>mt.cbFormat</b> member.


#### - dwStreamID

Stream identifier of the stream to process.


## -see-also




<a href="https://msdn.microsoft.com/218bf0c3-e618-4dcc-8618-34cd1fb5c0a8">AM_MPEGSYSTEMTYPE</a>



<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8">MEPG-1 Media Types</a>
 

 

