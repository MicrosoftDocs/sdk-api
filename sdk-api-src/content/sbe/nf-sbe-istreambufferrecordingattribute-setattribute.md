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

# IStreamBufferRecordingAttribute::SetAttribute


## -description


The <b>SetAttribute</b> method sets an attribute on the stream buffer file.


## -parameters




### -param ulReserved [in]

Reserved. Set this parameter to zero.


### -param pszAttributeName [in]

Wide-character string that contains the name of the attribute.


### -param StreamBufferAttributeType [in]

Member of the <a href="https://msdn.microsoft.com/be478769-d9ac-4e42-b5f6-94b5656e2596">STREAMBUFFER_ATTR_DATATYPE</a> enumeration that defines the data type of the attribute data.


### -param pbAttribute [in]

Pointer to a buffer that contains the attribute data.


### -param cbAttributeLength [in]

The size of the buffer specified in <i>pbAttribute</i>.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



If an attribute with that name already exists, the method overwrites it with the new value.

The method fails if the recorder object is already recording.




## -see-also




<a href="https://msdn.microsoft.com/e72ec34e-d3e3-4f5f-9336-d55135dc1e47">IStreamBufferRecordControl::Start</a>



<a href="https://msdn.microsoft.com/7c46413f-3e51-4d72-b7f7-a8239c61b161">IStreamBufferRecordingAttribute Interface</a>
 

 

