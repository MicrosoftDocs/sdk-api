---
UID: NN:spatialaudioclient.ISpatialAudioObjectBase
title: ISpatialAudioObjectBase (spatialaudioclient.h)
description: Base interface that represents an object that provides audio data to be rendered from a position in 3D space, relative to the user.
helpviewer_keywords: ["ISpatialAudioObjectBase","ISpatialAudioObjectBase interface [Core Audio]","ISpatialAudioObjectBase interface [Core Audio]","described","coreaudio.ispatialaudioobjectbase","spatialaudioclient/ISpatialAudioObjectBase"]
old-location: coreaudio\ispatialaudioobjectbase.htm
tech.root: CoreAudio
ms.assetid: 54721875-D93A-4C7E-A07E-C286E1A409D3
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectBase, ISpatialAudioObjectBase interface [Core Audio], ISpatialAudioObjectBase interface [Core Audio],described, coreaudio.ispatialaudioobjectbase, spatialaudioclient/ISpatialAudioObjectBase
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
 - ISpatialAudioObjectBase
 - spatialaudioclient/ISpatialAudioObjectBase
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
 - ISpatialAudioObjectBase
---

# ISpatialAudioObjectBase interface


## -description

Base interface that represents an object that provides audio data to  be  rendered from a position in 3D space, relative to the user. Spatial audio objects can be static or dynamic, which you specify with the <i>type</i> parameter to the  <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject</a> method. Dynamic audio objects can be placed in an arbitrary position in space and can be moved over time. Static audio objects are assigned to one or more channels, defined in the <a href="/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype">AudioObjectType</a> enumeration, that each correlate to a fixed speaker location that may be a physical or a virtualized speaker.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioObjectBase</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioObjectBase</b> also has these types of members:

