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
 

 

