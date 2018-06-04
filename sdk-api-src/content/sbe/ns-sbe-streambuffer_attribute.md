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

# STREAMBUFFER_ATTRIBUTE structure


## -description



This topic applies only to Windows XP Service Pack 1 or later.
          

The <b>STREAMBUFFER_ATTRIBUTE</b> structure describes an attribute on a stream buffer file.




## -struct-fields




### -field pszName

Pointer to a null-terminated wide-character string that contains the name of the attribute.


### -field StreamBufferAttributeType

Member of the <a href="https://msdn.microsoft.com/be478769-d9ac-4e42-b5f6-94b5656e2596">STREAMBUFFER_ATTR_DATATYPE</a> enumeration. The value indicates the data type that you should use to interpret the attribute data, which is contained in the <b>pbAttribute</b> member.


### -field pbAttribute

Pointer to a buffer that contains the attribute data.


### -field cbLength

The size of the buffer given in <b>pbAttribute</b>, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/760b2e2c-799d-45e5-9dbd-2407e7431918">IEnumStreamBufferRecordingAttrib::Next</a>



<a href="https://msdn.microsoft.com/90ac310a-7fd3-440f-9cf7-7d6eb58996cc">Stream Buffer Engine Structures</a>
 

 

