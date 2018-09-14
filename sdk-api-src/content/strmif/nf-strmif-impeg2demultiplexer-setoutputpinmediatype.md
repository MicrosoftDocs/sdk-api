---
UID: NF:strmif.IMpeg2Demultiplexer.SetOutputPinMediaType
title: IMpeg2Demultiplexer::SetOutputPinMediaType
author: windows-sdk-content
description: The SetOutputPinMediaType method updates the media type of the specified output pin. (DirectX 9.0 and later.).
old-location: dshow\impeg2demultiplexer_setoutputpinmediatype.htm
tech.root: DirectShow
ms.assetid: 985033ea-72ea-40c4-8176-60208b505040
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IMpeg2Demultiplexer interface [DirectShow],SetOutputPinMediaType method, IMpeg2Demultiplexer.SetOutputPinMediaType, IMpeg2Demultiplexer::SetOutputPinMediaType, IMpeg2DemultiplexerSetOutputPinMediaType, SetOutputPinMediaType, SetOutputPinMediaType method [DirectShow], SetOutputPinMediaType method [DirectShow],IMpeg2Demultiplexer interface, dshow.impeg2demultiplexer_setoutputpinmediatype, strmif/IMpeg2Demultiplexer::SetOutputPinMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMpeg2Demultiplexer.SetOutputPinMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMpeg2Demultiplexer::SetOutputPinMediaType


## -description



The <code>SetOutputPinMediaType</code> method updates the media type of the specified output pin. (DirectX 9.0 and later.)




## -parameters




### -param pszPinName [in]

The friendly name of the pin as specified when the pin was created in a call to <b>CreateOutputPin</b>.


### -param pMediaType [in]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that specifies the new media type information for the pin.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



Pins can be reconfigured at any time with a new media type. If no connection exists, the media type is simply updated. If the pin is connected, the success or failure of the call will depend on the downstream input pin's acceptance or rejection of the specified media type.

The media type is not interpreted in any way by the Demultiplexer filter. It is used only during connection negotiation by the output pin. It has no effect on the content of the media samples. Media sample content is defined when a PID is mapped via the MEDIA_SAMPLE_CONTENT parameter in the <a href="https://msdn.microsoft.com/22784e4a-2b02-4fc9-ba55-8c918ea38892">IMPEG2PIDMap::MapPID</a> method, or via the defined values in an <a href="https://msdn.microsoft.com/e74a1e62-1bc4-43e1-9017-85012b2ece01">IMPEG2StreamIdMap::MapStreamId</a> call.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e9242b96-0fc3-428e-b7ee-91a4f5e67305">IMpeg2Demultiplexer Interface</a>
 

 

