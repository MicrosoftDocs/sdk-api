---
UID: NF:strmif.IMpeg2Demultiplexer.SetOutputPinMediaType
title: IMpeg2Demultiplexer::SetOutputPinMediaType (strmif.h)
description: The SetOutputPinMediaType method updates the media type of the specified output pin. (DirectX 9.0 and later.).helpviewer_keywords: ["IMpeg2Demultiplexer interface [DirectShow]","SetOutputPinMediaType method","IMpeg2Demultiplexer.SetOutputPinMediaType","IMpeg2Demultiplexer::SetOutputPinMediaType","IMpeg2DemultiplexerSetOutputPinMediaType","SetOutputPinMediaType","SetOutputPinMediaType method [DirectShow]","SetOutputPinMediaType method [DirectShow]","IMpeg2Demultiplexer interface","dshow.impeg2demultiplexer_setoutputpinmediatype","strmif/IMpeg2Demultiplexer::SetOutputPinMediaType"]
old-location: dshow\impeg2demultiplexer_setoutputpinmediatype.htm
tech.root: DirectShow
ms.assetid: 985033ea-72ea-40c4-8176-60208b505040
ms.date: 12/05/2018
ms.keywords: IMpeg2Demultiplexer interface [DirectShow],SetOutputPinMediaType method, IMpeg2Demultiplexer.SetOutputPinMediaType, IMpeg2Demultiplexer::SetOutputPinMediaType, IMpeg2DemultiplexerSetOutputPinMediaType, SetOutputPinMediaType, SetOutputPinMediaType method [DirectShow], SetOutputPinMediaType method [DirectShow],IMpeg2Demultiplexer interface, dshow.impeg2demultiplexer_setoutputpinmediatype, strmif/IMpeg2Demultiplexer::SetOutputPinMediaType
f1_keywords:
- strmif/IMpeg2Demultiplexer.SetOutputPinMediaType
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMpeg2Demultiplexer::SetOutputPinMediaType


## -description



The <code>SetOutputPinMediaType</code> method updates the media type of the specified output pin. (DirectX 9.0 and later.)




## -parameters




### -param pszPinName [in]

The friendly name of the pin as specified when the pin was created in a call to <b>CreateOutputPin</b>.


### -param pMediaType [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that specifies the new media type information for the pin.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



Pins can be reconfigured at any time with a new media type. If no connection exists, the media type is simply updated. If the pin is connected, the success or failure of the call will depend on the downstream input pin's acceptance or rejection of the specified media type.

The media type is not interpreted in any way by the Demultiplexer filter. It is used only during connection negotiation by the output pin. It has no effect on the content of the media samples. Media sample content is defined when a PID is mapped via the MEDIA_SAMPLE_CONTENT parameter in the <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-impeg2pidmap-mappid">IMPEG2PIDMap::MapPID</a> method, or via the defined values in an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-impeg2streamidmap-mapstreamid">IMPEG2StreamIdMap::MapStreamId</a> call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-impeg2demultiplexer">IMpeg2Demultiplexer Interface</a>
 

 

