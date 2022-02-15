---
UID: NN:spatialaudioclient.ISpatialAudioObjectRenderStream
title: ISpatialAudioObjectRenderStream (spatialaudioclient.h)
description: Provides methods for controlling a spatial audio object render stream, including starting, stopping, and resetting the stream.
helpviewer_keywords: ["ISpatialAudioObjectRenderStream","ISpatialAudioObjectRenderStream interface [Core Audio]","ISpatialAudioObjectRenderStream interface [Core Audio]","described","coreaudio.ispatialaudioobjectrenderstream","spatialaudioclient/ISpatialAudioObjectRenderStream"]
old-location: coreaudio\ispatialaudioobjectrenderstream.htm
tech.root: CoreAudio
ms.assetid: B4D10CC6-62BF-4D20-910F-E39DF812010D
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectRenderStream, ISpatialAudioObjectRenderStream interface [Core Audio], ISpatialAudioObjectRenderStream interface [Core Audio],described, coreaudio.ispatialaudioobjectrenderstream, spatialaudioclient/ISpatialAudioObjectRenderStream
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpatialAudioObjectRenderStream
 - spatialaudioclient/ISpatialAudioObjectRenderStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStream
---

# ISpatialAudioObjectRenderStream interface


## -description

Provides methods for controlling a spatial audio object render stream, including starting, stopping, and resetting the stream. Also provides methods for activating new <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> instances and notifying the system when you are beginning and ending the process of updating activated spatial audio objects and data.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioObjectRenderStream</b> interface inherits from <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a>. <b>ISpatialAudioObjectRenderStream</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a> interface.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a>
