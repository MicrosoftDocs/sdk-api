---
UID: NN:spatialaudiohrtf.ISpatialAudioObjectForHrtf
title: ISpatialAudioObjectForHrtf (spatialaudiohrtf.h)
description: Represents an object that provides audio data to be rendered from a position in 3D space, relative to the user, a head-relative transfer function (HRTF).
helpviewer_keywords: ["ISpatialAudioObjectForHrtf","ISpatialAudioObjectForHrtf interface [Core Audio]","ISpatialAudioObjectForHrtf interface [Core Audio]","described","coreaudio.ispatialaudioobjectforhrtf","spatialaudiohrtf/ISpatialAudioObjectForHrtf"]
old-location: coreaudio\ispatialaudioobjectforhrtf.htm
tech.root: CoreAudio
ms.assetid: E69F1D09-B937-4BCC-A040-18EF8A838289
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectForHrtf, ISpatialAudioObjectForHrtf interface [Core Audio], ISpatialAudioObjectForHrtf interface [Core Audio],described, coreaudio.ispatialaudioobjectforhrtf, spatialaudiohrtf/ISpatialAudioObjectForHrtf
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
 - ISpatialAudioObjectForHrtf
 - spatialaudiohrtf/ISpatialAudioObjectForHrtf
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
 - ISpatialAudioObjectForHrtf
---

# ISpatialAudioObjectForHrtf interface


## -description

Represents an object that provides audio data to  be  rendered from a position in 3D space, relative to the user, a head-relative transfer function (HRTF). Spatial audio objects can be static or dynamic, which you specify with the <i>type</i> parameter to the <a href="/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf">ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf</a>   method. Dynamic audio objects can be placed in an arbitrary position in space and can be moved over time. Static audio objects are assigned to one or more channels, defined in the <a href="/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype">AudioObjectType</a> enumeration, that each correlate to a fixed speaker location that may be a physical or a virtualized speaker

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioObjectForHrtf</b> interface inherits from <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a>. <b>ISpatialAudioObjectForHrtf</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a> interface.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a>
