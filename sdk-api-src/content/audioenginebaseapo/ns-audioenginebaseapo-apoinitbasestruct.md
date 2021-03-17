---
UID: NS:audioenginebaseapo.APOInitBaseStruct
title: APOInitBaseStruct (audioenginebaseapo.h)
description: The APOInitBaseStruct structure is the base initialization header that must precede other initialization data in IAudioProcessingObject::Initialize.
helpviewer_keywords: ["APOInitBaseStruct","APOInitBaseStruct structure [Audio Devices]","PAPOInitBaseStruct","PAPOInitBaseStruct structure pointer [Audio Devices]","audio.apoinitbasestruct","audioenginebaseapo/APOInitBaseStruct","audioenginebaseapo/PAPOInitBaseStruct"]
old-location: audio\apoinitbasestruct.htm
tech.root: audio
ms.assetid: 15C973AE-B0E8-42FD-9F34-671A6A915B47
ms.date: 12/05/2018
ms.keywords: APOInitBaseStruct, APOInitBaseStruct structure [Audio Devices], PAPOInitBaseStruct, PAPOInitBaseStruct structure pointer [Audio Devices], audio.apoinitbasestruct, audioenginebaseapo/APOInitBaseStruct, audioenginebaseapo/PAPOInitBaseStruct
req.header: audioenginebaseapo.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: APOInitBaseStruct
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APOInitBaseStruct
 - audioenginebaseapo/APOInitBaseStruct
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audioenginebaseapo.h
api_name:
 - APOInitBaseStruct
---

# APOInitBaseStruct structure


## -description

The APOInitBaseStruct structure is the base initialization header that must precede other  
initialization data in <a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-initialize">IAudioProcessingObject::Initialize</a>.

## -struct-fields

### -field cbSize

The total size of the structure in bytes.

### -field clsid

The Class ID (CLSID) of the APO.

## -remarks

If the specified CLSID does not match, then the APOInitBaseStruct structure was not designed for this APO, and this is an error condition.  And if the CLSID of the APO changes  
    between versions, then the CLSID may also be used for version management.  In the case where the CLSID is used for version management, a previous version may still be supported by the APO.

## -see-also

<a href="/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects">APOInitSystemEffects</a>



<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-initialize">IAudioProcessingObject::Initialize</a>