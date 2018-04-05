---
UID: NE:mmstream.__MIDL___MIDL_itf_mmstream_0000_0000_0002
title: "__MIDL___MIDL_itf_mmstream_0000_0000_0002"
author: windows-driver-content
description: Note  This API is deprecated. New applications should not use it. Describes the state of the stream.
old-location: dshow\stream_state.htm
old-project: DirectShow
ms.assetid: 0be95819-0a42-4459-a891-194aacd26e2e
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: STREAMSTATE_RUN, STREAMSTATE_STOP, STREAM_STATE, STREAM_STATE enumeration [DirectShow], __MIDL___MIDL_itf_mmstream_0000_0000_0002, dshow.stream_state, mmstream/STREAMSTATE_RUN, mmstream/STREAMSTATE_STOP, mmstream/STREAM_STATE
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
req.typenames: STREAM_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mmstream.h
api_name:
-	STREAM_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mmstream_0000_0000_0002 enumeration


## -description



<div class="alert"><b>Note</b>  This API is deprecated. New applications should not use it.</div>
<div> </div>
Describes the state of the stream.




## -enum-fields




### -field STREAMSTATE_STOP

Stop state.


### -field STREAMSTATE_RUN

Run state.


## -remarks



Change the state by calling the <a href="https://msdn.microsoft.com/69c3612f-e91a-4ab3-8f6d-2966e64a9220">IMultiMediaStream::SetState</a> method.




## -see-also




<a href="https://msdn.microsoft.com/0b2866cc-ff07-4cd9-b7df-6a05436251d3">Multimedia Streaming Enumeration Types</a>
 

 

