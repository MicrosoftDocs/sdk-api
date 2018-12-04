---
UID: NE:codecapi.eAVEncMuxOutput
title: eAVEncMuxOutput
author: windows-sdk-content
description: Specifies the type of output stream produced by a multiplexer. This enumeration is used with the AVEncMuxOutputStreamType property.
old-location: dshow\eavencmuxoutput.htm
tech.root: DirectShow
ms.assetid: 2020192d-0db1-41e0-b03f-d5a7dbc85106
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: codecapi/eAVEncMuxOutput, codecapi/eAVEncMuxOutputAuto, codecapi/eAVEncMuxOutputPS, codecapi/eAVEncMuxOutputTS, dshow.eavencmuxoutput, eAVEncMuxOutput, eAVEncMuxOutput enumeration [DirectShow], eAVEncMuxOutputAuto, eAVEncMuxOutputPS, eAVEncMuxOutputTS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVEncMuxOutput enumeration


## -description



Specifies the type of output stream produced by a multiplexer. This enumeration is used with the <a href="https://msdn.microsoft.com/c3ee20b9-cae9-4a84-b173-3a4919202b3d">AVEncMuxOutputStreamType</a> property.




## -enum-fields




### -field eAVEncMuxOutputAuto

The multiplexer automatically selects whether to output an elementary stream, a program stream, or  a transport stream.


### -field eAVEncMuxOutputPS

The multiplexer outputs a program stream.


### -field eAVEncMuxOutputTS

The multiplexer outputs a transport stream.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

