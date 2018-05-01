---
UID: NE:mmstream.__MIDL___MIDL_itf_mmstream_0000_0000_0001
title: "__MIDL___MIDL_itf_mmstream_0000_0000_0001"
author: windows-driver-content
description: Note  This API is deprecated. New applications should not use it. Defines the direction of data flow for the stream.
old-location: dshow\stream_type.htm
old-project: DirectShow
ms.assetid: 07ab5ded-28b8-4cac-b4da-76f07ad351ef
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: STREAMTYPE_READ, STREAMTYPE_TRANSFORM, STREAMTYPE_WRITE, STREAM_TYPE, STREAM_TYPE enumeration [DirectShow], __MIDL___MIDL_itf_mmstream_0000_0000_0001, dshow.stream_type, mmstream/STREAMTYPE_READ, mmstream/STREAMTYPE_TRANSFORM, mmstream/STREAMTYPE_WRITE, mmstream/STREAM_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mmstream.h
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
req.typenames: STREAM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mmstream.h
api_name:
-	STREAM_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mmstream_0000_0000_0001 enumeration


## -description



<div class="alert"><b>Note</b>  This API is deprecated. New applications should not use it.</div>
<div> </div>
Defines the direction of data flow for the stream.




## -enum-fields




### -field STREAMTYPE_READ

Application can read the stream.


### -field STREAMTYPE_WRITE

Application can write to the stream.


### -field STREAMTYPE_TRANSFORM

Application reads and writes to the stream. 


## -remarks



Transform streams are read/write where the sample is updated in place.




## -see-also




<a href="https://msdn.microsoft.com/0b2866cc-ff07-4cd9-b7df-6a05436251d3">Multimedia Streaming Enumeration Types</a>
 

 

