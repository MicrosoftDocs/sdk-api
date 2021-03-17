---
UID: NS:devicetopology._tagKSJACK_DESCRIPTION2
title: KSJACK_DESCRIPTION2 (devicetopology.h)
description: The KSJACK_DESCRIPTION2 structure describes an audio jack.To get the description of an audio jack of a connector, call IKsJackDescription2::GetJackDescription2.
helpviewer_keywords: ["*PKSJACK_DESCRIPTION2","KSJACK_DESCRIPTION2","KSJACK_DESCRIPTION2 structure [Core Audio]","PKSJACK_DESCRIPTION2","PKSJACK_DESCRIPTION2 structure pointer [Core Audio]","coreaudio.ksjack_description2","devicetopology/KSJACK_DESCRIPTION2","devicetopology/PKSJACK_DESCRIPTION2"]
old-location: coreaudio\ksjack_description2.htm
tech.root: CoreAudio
ms.assetid: 67714767-24b8-4838-953a-d6aca0c55bbb
ms.date: 12/05/2018
ms.keywords: '*PKSJACK_DESCRIPTION2, KSJACK_DESCRIPTION2, KSJACK_DESCRIPTION2 structure [Core Audio], PKSJACK_DESCRIPTION2, PKSJACK_DESCRIPTION2 structure pointer [Core Audio], coreaudio.ksjack_description2, devicetopology/KSJACK_DESCRIPTION2, devicetopology/PKSJACK_DESCRIPTION2'
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: KSJACK_DESCRIPTION2, *PKSJACK_DESCRIPTION2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagKSJACK_DESCRIPTION2
 - devicetopology/_tagKSJACK_DESCRIPTION2
 - PKSJACK_DESCRIPTION2
 - devicetopology/PKSJACK_DESCRIPTION2
 - KSJACK_DESCRIPTION2
 - devicetopology/KSJACK_DESCRIPTION2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Devicetopology.h
api_name:
 - KSJACK_DESCRIPTION2
---

# KSJACK_DESCRIPTION2 structure


## -description

The <b>KSJACK_DESCRIPTION2</b> structure describes an audio jack.

To get the description of an audio jack of a connector, call <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2">IKsJackDescription2::GetJackDescription2</a>.

## -struct-fields

### -field DeviceStateInfo

Reserved for future use.

### -field JackCapabilities

Stores the audio jack's capabilities: jack presence detection capability 
                                       or dynamic format changing capability. The constants that can be stored in this member of the structure are defined in Ksmedia.h as follows:

<ul>
<li>JACKDESC2_PRESENCE_DETECT_CAPABILITY       (0x00000001)</li>
<li>JACKDESC2_DYNAMIC_FORMAT_CHANGE_CAPABILITY (0x00000002)
</li>
</ul>

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-structures">Core Audio Structures</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksjackdescription2">IKsJackDescription2</a>