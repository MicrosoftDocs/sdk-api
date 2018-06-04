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

# _MT_ARBITRARY_HEADER structure


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
          <a href="https://msdn.microsoft.com/fc5b9890-1508-498e-b2ce-ed4fa2052f9c">MF_MT_ARBITRARY_FORMAT</a> attribute of the media type. If no additional format data is present, <b>formattype</b> equals GUID_NULL.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/45608dde-894b-4204-80dc-505f068fb158">MF_MT_ARBITRARY_HEADER</a> media type attribute.

This structure corresponds to the first 60 bytes of the Type-Specific Data field of the Stream Properties Object, in files where the stream type is ASF_Binary_Media. For more information, see the ASF specification.

The Format Data field of the Type-Specific Data field is contained in the <a href="https://msdn.microsoft.com/fc5b9890-1508-498e-b2ce-ed4fa2052f9c">MF_MT_ARBITRARY_FORMAT</a> attribute of the media type.




## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

