---
UID: NS:audioenginebaseapo.APO_REG_PROPERTIES
title: APO_REG_PROPERTIES (audioenginebaseapo.h)
description: The APO_REG_PROPERTIES structure is used by IAudioProcessingObject::GetRegistrationProperties for returning the registration properties of an audio processing object (APO).
helpviewer_keywords: ["*PAPO_REG_PROPERTIES","APO_REG_PROPERTIES","APO_REG_PROPERTIES structure [Audio Devices]","PAPO_REG_PROPERTIES","PAPO_REG_PROPERTIES structure pointer [Audio Devices]","audio.apo_reg_properties","audioenginebaseapo/APO_REG_PROPERTIES","audioenginebaseapo/PAPO_REG_PROPERTIES"]
old-location: audio\apo_reg_properties.htm
tech.root: audio
ms.assetid: 466215E5-5345-4570-A29B-086562882F5D
ms.date: 12/05/2018
ms.keywords: '*PAPO_REG_PROPERTIES, APO_REG_PROPERTIES, APO_REG_PROPERTIES structure [Audio Devices], PAPO_REG_PROPERTIES, PAPO_REG_PROPERTIES structure pointer [Audio Devices], audio.apo_reg_properties, audioenginebaseapo/APO_REG_PROPERTIES, audioenginebaseapo/PAPO_REG_PROPERTIES'
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
req.typenames: APO_REG_PROPERTIES, *PAPO_REG_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APO_REG_PROPERTIES
 - audioenginebaseapo/APO_REG_PROPERTIES
 - PAPO_REG_PROPERTIES
 - audioenginebaseapo/PAPO_REG_PROPERTIES
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
 - APO_REG_PROPERTIES
---

# APO_REG_PROPERTIES structure


## -description

The APO_REG_PROPERTIES structure is used by <a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-getregistrationproperties">IAudioProcessingObject::GetRegistrationProperties</a> for returning the registration properties of  an audio processing object (APO).

## -struct-fields

### -field clsid

The class ID for this APO.

### -field Flags

The flags for this APO. This parameter is an enumerated constant of type <a href="/windows/desktop/api/audioenginebaseapo/ne-audioenginebaseapo-apo_flag">APO_FLAG</a>.

### -field szFriendlyName

The friendly name of this APO. This is a string of characters with a max length of 256.

### -field szCopyrightInfo

The copyright info for this APO. This is a string of characters with a max length of 256.

### -field u32MajorVersion

The major version number for this APO.

### -field u32MinorVersion

The minor version number for this APO.

### -field u32MinInputConnections

The minimum number of input connections for this APO.

### -field u32MaxInputConnections

The maximum number of input connections for this APO.

### -field u32MinOutputConnections

The minimum number of output connections for this APO.

### -field u32MaxOutputConnections

The maximum number of output connections for this APO.

### -field u32MaxInstances

The maximum number of instances of this APO.

### -field u32NumAPOInterfaces

The number of interfaces for this APO.

### -field iidAPOInterfaceList

## -see-also

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-getregistrationproperties">IAudioProcessingObject::GetRegistrationProperties</a>