---
UID: NN:spatialaudiohrtf.ISpatialAudioObjectRenderStreamForHrtf
title: ISpatialAudioObjectRenderStreamForHrtf (spatialaudiohrtf.h)
description: Provides methods for controlling an Hrtf spatial audio object render stream, including starting, stopping, and resetting the stream.
helpviewer_keywords: ["ISpatialAudioObjectRenderStreamForHrtf","ISpatialAudioObjectRenderStreamForHrtf interface [Core Audio]","ISpatialAudioObjectRenderStreamForHrtf interface [Core Audio]","described","coreaudio.ispatialaudiorenderstreamforhrtf","spatialaudiohrtf/ISpatialAudioObjectRenderStreamForHrtf"]
old-location: coreaudio\ispatialaudiorenderstreamforhrtf.htm
tech.root: CoreAudio
ms.assetid: 9DFEF82A-1571-47AB-BE0E-059BCCC8289A
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectRenderStreamForHrtf, ISpatialAudioObjectRenderStreamForHrtf interface [Core Audio], ISpatialAudioObjectRenderStreamForHrtf interface [Core Audio],described, coreaudio.ispatialaudiorenderstreamforhrtf, spatialaudiohrtf/ISpatialAudioObjectRenderStreamForHrtf
req.header: spatialaudiohrtf.h
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
 - ISpatialAudioObjectRenderStreamForHrtf
 - spatialaudiohrtf/ISpatialAudioObjectRenderStreamForHrtf
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudiohrtf.h
api_name:
 - ISpatialAudioObjectRenderStreamForHrtf
---

# ISpatialAudioObjectRenderStreamForHrtf interface


## -description

Provides methods for controlling an Hrtf spatial audio object render stream, including starting, stopping, and resetting the stream. Also provides methods for activating new <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> instances and notifying the system when you are beginning and ending the process of updating activated spatial audio objects and data.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioObjectRenderStreamForHrtf</b> interface inherits from <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a>. <b>ISpatialAudioObjectRenderStreamForHrtf</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a> interface.</div>
<div> </div>

## -see-also

<a href="../spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase.md">ISpatialAudioObjectRenderStreamBase</a>
