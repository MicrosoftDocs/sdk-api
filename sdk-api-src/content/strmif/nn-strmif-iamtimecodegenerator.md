---
UID: NN:strmif.IAMTimecodeGenerator
title: IAMTimecodeGenerator (strmif.h)
description: The IAMTimecodeGenerator interface controls how an external SMPTE/MIDI timecode generator supplies data to the filter graph.DirectShow currently does not provide any filters that implement this interface.
helpviewer_keywords: ["IAMTimecodeGenerator","IAMTimecodeGenerator interface [DirectShow]","IAMTimecodeGenerator interface [DirectShow]","described","IAMTimecodeGeneratorInterface","dshow.iamtimecodegenerator","strmif/IAMTimecodeGenerator"]
old-location: dshow\iamtimecodegenerator.htm
tech.root: dshow
ms.assetid: 7fe74fc2-03bd-43dd-917f-ee0149f1e17f
ms.date: 12/05/2018
ms.keywords: IAMTimecodeGenerator, IAMTimecodeGenerator interface [DirectShow], IAMTimecodeGenerator interface [DirectShow],described, IAMTimecodeGeneratorInterface, dshow.iamtimecodegenerator, strmif/IAMTimecodeGenerator
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTimecodeGenerator
 - strmif/IAMTimecodeGenerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTimecodeGenerator
---

# IAMTimecodeGenerator interface


## -description

The <code>IAMTimecodeGenerator</code> interface controls how an external SMPTE/MIDI timecode generator supplies data to the filter graph.

DirectShow currently does not provide any filters that implement this interface. Third parties should implement this interface on any filter that controls an external timecode generator. Timecode generators can be built into a VCR or can be separate external devices. The device must be able to read timecode and send it to the computer over its control interface. If not, the user must have a timecode reader card in the computer, or you can write a software decoder that converts VITC embedded in captured video frames or LTC captured as an audio signal into DirectShow timecode samples.

SMPTE timecode is a frame addressing system that identifies video and audio sources, makes automatic track synchronization possible, and provides a container for additional data related to the production. SMPTE timecode's main purpose is to provide a machine-readable address for video and audio. It is displayed in hh:mm:ss:ff format and is thoroughly defined in ANSI/SMPTE 12-1986.

Optionally, you can enable applications to convert timecode to reference time by supporting the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-converttimeformat">IMediaSeeking::ConvertTimeFormat</a> method on the filter.

<b>Hardware Requirements</b>

For hardware requirements, see the <a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport</a> interface.

## -inheritance

The <b>IAMTimecodeGenerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMTimecodeGenerator</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodereader">IAMTimecodeReader Interface</a>
