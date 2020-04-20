---
UID: NE:codecapi.eAVEncMuxOutput
title: eAVEncMuxOutput (codecapi.h)
description: Specifies the type of output stream produced by a multiplexer. This enumeration is used with the AVEncMuxOutputStreamType property.helpviewer_keywords: ["codecapi/eAVEncMuxOutput","codecapi/eAVEncMuxOutputAuto","codecapi/eAVEncMuxOutputPS","codecapi/eAVEncMuxOutputTS","dshow.eavencmuxoutput","eAVEncMuxOutput","eAVEncMuxOutput enumeration [DirectShow]","eAVEncMuxOutputAuto","eAVEncMuxOutputPS","eAVEncMuxOutputTS"]
old-location: dshow\eavencmuxoutput.htm
tech.root: DirectShow
ms.assetid: 2020192d-0db1-41e0-b03f-d5a7dbc85106
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncMuxOutput, codecapi/eAVEncMuxOutputAuto, codecapi/eAVEncMuxOutputPS, codecapi/eAVEncMuxOutputTS, dshow.eavencmuxoutput, eAVEncMuxOutput, eAVEncMuxOutput enumeration [DirectShow], eAVEncMuxOutputAuto, eAVEncMuxOutputPS, eAVEncMuxOutputTS
f1_keywords:
- codecapi/eAVEncMuxOutput
dev_langs:
- c++
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
- codecapi.h
api_name:
- eAVEncMuxOutput
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVEncMuxOutput enumeration


## -description



Specifies the type of output stream produced by a multiplexer. This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avencmuxoutputstreamtype">AVEncMuxOutputStreamType</a> property.




## -enum-fields




### -field eAVEncMuxOutputAuto

The multiplexer automatically selects whether to output an elementary stream, a program stream, or  a transport stream.


### -field eAVEncMuxOutputPS

The multiplexer outputs a program stream.


### -field eAVEncMuxOutputTS

The multiplexer outputs a transport stream.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 

