---
UID: NE:audioenginebaseapo.APO_FLAG
title: APO_FLAG (audioenginebaseapo.h)
description: The APO_FLAG enumeration defines constants that are used as flags by an audio processing object (APO).
helpviewer_keywords: ["APO_FLAG","APO_FLAG enumeration [Audio Devices]","APO_FLAG_BITSPERSAMPLE_MUST_MATCH","APO_FLAG_DEFAULT","APO_FLAG_FRAMESPERSECOND_MUST_MATCH","APO_FLAG_INPLACE","APO_FLAG_NONE","APO_FLAG_SAMPLESPERFRAME_MUST_MATCH","audio.apo_flag","audioenginebaseapo/APO_FLAG","audioenginebaseapo/APO_FLAG_BITSPERSAMPLE_MUST_MATCH","audioenginebaseapo/APO_FLAG_DEFAULT","audioenginebaseapo/APO_FLAG_FRAMESPERSECOND_MUST_MATCH","audioenginebaseapo/APO_FLAG_INPLACE","audioenginebaseapo/APO_FLAG_NONE","audioenginebaseapo/APO_FLAG_SAMPLESPERFRAME_MUST_MATCH"]
old-location: audio\apo_flag.htm
tech.root: audio
ms.assetid: 42134625-A351-4CB6-B83C-3F2E662D1938
ms.date: 12/05/2018
ms.keywords: APO_FLAG, APO_FLAG enumeration [Audio Devices], APO_FLAG_BITSPERSAMPLE_MUST_MATCH, APO_FLAG_DEFAULT, APO_FLAG_FRAMESPERSECOND_MUST_MATCH, APO_FLAG_INPLACE, APO_FLAG_NONE, APO_FLAG_SAMPLESPERFRAME_MUST_MATCH, audio.apo_flag, audioenginebaseapo/APO_FLAG, audioenginebaseapo/APO_FLAG_BITSPERSAMPLE_MUST_MATCH, audioenginebaseapo/APO_FLAG_DEFAULT, audioenginebaseapo/APO_FLAG_FRAMESPERSECOND_MUST_MATCH, audioenginebaseapo/APO_FLAG_INPLACE, audioenginebaseapo/APO_FLAG_NONE, audioenginebaseapo/APO_FLAG_SAMPLESPERFRAME_MUST_MATCH
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: APO_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APO_FLAG
 - audioenginebaseapo/APO_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - audioenginebaseapo.h
api_name:
 - APO_FLAG
---

# APO_FLAG enumeration


## -description

The APO_FLAG enumeration defines constants that are used as flags by an audio processing object (APO).

This enumeration is used by the <a href="/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apo_reg_properties">APO_REG_PROPERTIES</a> structure to help describe the registration properties of an APO.

## -enum-fields

### -field APO_FLAG_NONE

Indicates that there are no flags enabled for this APO.

### -field APO_FLAG_INPLACE

Indicates that this APO can perform in-place processing. This allows the processor to use a common buffer for input and output.

### -field APO_FLAG_SAMPLESPERFRAME_MUST_MATCH

Indicates that the samples per frame for the input and output connections must match.

### -field APO_FLAG_FRAMESPERSECOND_MUST_MATCH

Indicates that the frames per second for the input and output connections must match.

### -field APO_FLAG_BITSPERSAMPLE_MUST_MATCH

Indicates that bits per sample AND bytes per sample container for the  input and output connections must match.

### -field APO_FLAG_MIXER

### -field APO_FLAG_DEFAULT

The value of this member is determined by the logical OR result of the three preceding members. In other words:

APO_FLAG_DEFAULT = ( APO_FLAG_SAMPLESPERFRAME_MUST_MATCH | APO_FLAG_FRAMESPERSECOND_MUST_MATCH | APO_FLAG_BITSPERSAMPLE_MUST_MATCH ).

## -see-also

<a href="/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apo_reg_properties">APO_REG_PROPERTIES</a>