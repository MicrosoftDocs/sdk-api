---
UID: NS:sbe.STREAMBUFFER_ATTRIBUTE
title: STREAMBUFFER_ATTRIBUTE (sbe.h)
author: windows-sdk-content
description: This topic applies only to Windows XP Service Pack 1 or later. The STREAMBUFFER_ATTRIBUTE structure describes an attribute on a stream buffer file.
old-location: mstv\streambuffer_attribute.htm
tech.root: mstv
ms.assetid: 2b17626a-9268-4192-8acf-ed46bf632163
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: STREAMBUFFER_ATTRIBUTE, STREAMBUFFER_ATTRIBUTE structure [Microsoft TV Technologies], STREAMBUFFER_ATTRIBUTEStructure, mstv.streambuffer_attribute, sbe/STREAMBUFFER_ATTRIBUTE
ms.topic: struct
req.header: sbe.h
req.include-header: 
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
 - Sbe.h
api_name:
 - STREAMBUFFER_ATTRIBUTE
product: Windows
targetos: Windows
req.typenames: STREAMBUFFER_ATTRIBUTE
req.redist: 
ms.custom: 19H1
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
 

 

